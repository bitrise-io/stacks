---
title: Defining tool versions for reliable builds
type: basic_page
---

Multiple versions are installed of tools like Ruby, Node.js and Go on the stacks side-by-side. Since most projects depend on a specific version (implicitly or explicitly), it's a good idea to declare the required version in workflows instead of relying on the default version available in `$PATH`.

{{< hint info >}}
Installed tool versions are listed in the stack reports ([example]({{< ref "/stack_reports/osx-xcode-14.3.x-ventura.md" >}}))
{{< /hint >}}

Bitrise helps selecting the right tool version in three ways:

1. Common configuration options like the `.ruby-version` file or the `$NODE_VERSION` environment variable are automatically recognized during the build. The version declared with these options is automatically activated (if available installed). This is implemented with the [asdf](https://asdf-vm.com/) project.
2. Additional versions can be installed at runtime with a single command like `asdf install ruby 3.2.0`
3. Some Bitrise steps that depend on a tool - such as the Cocoapods or Fastlane steps - install the declared version automatically (if not available)

### How to declare tool versions
The best way to declare the specific tool version is via version files like `.ruby-version`, `.node-version`, `.tool-versions`, etc. By storing this information in the project repository, every developer's local environment can match the CI environment by using a version manager (we recommend [asdf](https://asdf-vm.com/), which handles the most common tools in one version manager).

The following version files are automatically recognized in Bitrise stacks:

- `.tool-versions` ([learn more](https://asdf-vm.com/manage/configuration.html#tool-versions))
- `.ruby-version`
- `.node-version`
- `.nvmrc`
- `.go-version`

By placing this file in the repository root, commands executed in that directory (or its subfolders) will see the declared tool version in `$PATH`.

Changing a version at runtime is also possible via the asdf CLI tool, for example:

```sh
asdf local ruby 3.2
asdf local nodejs 18.16
```

### Version aliases
Not every possible tool version is preinstalled on the stacks, but there are special alias versions defined for every `major` and `major.minor` version. These aliases always point to the latest installed patch version and can be used like full version numbers.
For example, declaring Ruby `3.2` selects one preinstalled Ruby version, the latest available patch version of `3.2.x`.

{{< hint warning >}}
Because patch versions are sometimes upgraded (replaced in-place) on Bitrise stacks for critical bugfixes, we recommend declaring one of the alias versions (`major` or `major.minor`) in your project.
The implementation of version aliases is based on the [ASDF alias plugin](https://github.com/andrewthauer/asdf-alias), which you can set up in the local environment too.
{{< /hint >}}

### Debugging version selection issues
To see what are the currently selected tool versions and why, run `asdf current` in a script step:

```
golang          1.20            /Users/vagrant/.tool-versions
nodejs          18              /Users/vagrant/workspace/.node-version
ruby            3.2             /Users/vagrant/.tool-versions
```
This shows that Go and Ruby versions are coming from the global `.tool-versions` file in the user home, while the Node.js version is coming from the current folder's `.node-version` file.
