---
title: Defining tool versions for reliable builds
type: basic_page
---

Bitrise stacks are shared environments: they come with a curated set of common tools and versions preinstalled, but every project has its own requirements. Just like pinning dependency versions in a lockfile, explicitly declaring which tool versions your build needs makes it reproducible and protects it from unexpected breakage when the stack is updated or when you switch to a newer stack.

Multiple versions of tools like Ruby, Node.js, Go, and Python are installed side-by-side on Bitrise stacks, so declaring the required version activates the right one rather than relying on whatever happens to be the default.

Bitrise has [a native tool version setup feature](https://docs.bitrise.io/en/bitrise-ci/configure-builds/configuring-build-settings/configuring-tool-versions.html) that provides the smoothest experience: you can configure tools either in YML, CLI or a step form, and Bitrise makes sure that tool installs are fast and reliable. If you prefer, you can also bring your own version manager of choice (mise, rvm, nvm, etc.) and manage versions yourself.

Installed tool versions are listed in the stack reports ([example]({{< ref "/stack_reports/osx-xcode-26.0.x.md" >}})).

### Native declarative setup (recommended)

Declare required tools and versions in the `tools` property at the top level of your `bitrise.yml`. Bitrise resolves and activates them automatically before the first workflow step runs.

Supported tools include Ruby, Go, Python, Node.js, Java, Flutter, Tuist, and many more. Versions can be specified exactly (`3.2.0`), partially (`3.2:installed`, `3.2:latest`), or with the `latest` and `installed` aliases. Tools can also be overridden or unset per workflow.

```yaml
tools:
  nodejs: 22:latest
  ruby: 3.3:installed
  golang: 1.24.5

workflows:
  test-latest-node:
    tools:
      nodejs: "24.7.0"   # override for this workflow only
```

[Full documentation on declarative tool setup →](https://docs.bitrise.io/en/bitrise-ci/configure-builds/configuring-build-settings/configuring-tool-versions.html#declarative-tool-setup)

### Installing tools at runtime

As an alternative to the declarative setup, tools can also be activated during workflow execution using the `bitrise tools setup` CLI subcommand or the **Dependency Installer** Step. This is particularly useful when tool versions are defined in committed version files, since the declarative setup runs before the Git Clone step.

Via the CLI in a Script step:

```bash
eval "$(bitrise tools install nodejs 22:latest --format bash)"
```

Or via the Dependency Installer Step:

```yaml
steps:
  - git-clone@8: {}
  - dependency-installer@1:
      inputs:
        - tool_version_file: ".tool-versions"
```

[Full documentation on runtime tool setup →](https://docs.bitrise.io/en/bitrise-ci/configure-builds/configuring-build-settings/configuring-tool-versions.html#tool-setup-during-workflow-execution)

### Version files

The `bitrise tools setup` CLI command can be called in a Script step to activate tools and their versions for the current workflow session. When called from the repository root, version files like `.ruby-version`, `.node-version`, `.nvmrc`, `.tool-versions`, and `.go-version` are automatically detected and respected. This is useful for keeping local dev environments in sync with CI without duplicating version declarations.

```bash
# .tool-versions
nodejs 22.1.0
ruby 3.3.0
golang 1.24.5
```

```bash
eval "$(bitrise tools setup --config .tool-versions --format bash)"
```
