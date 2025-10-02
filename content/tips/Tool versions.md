---
title: Defining tool versions for reliable builds
type: basic_page
---

Multiple versions are installed of tools like Ruby, Node.js and Go on the stacks side-by-side. Since most projects depend on a specific version (implicitly or explicitly), it's a good idea to declare the required version in workflows instead of relying on the default version available in `$PATH`.

{{< hint info >}}
Installed tool versions are listed in the stack reports ([example]({{< ref "/stack_reports/osx-xcode-26.0.x.md" >}}))
{{< /hint >}}

Bitrise helps selecting the right tool version in three ways:

1. Common configuration options like the `.ruby-version` file or the `$NODE_VERSION` environment variable are automatically recognized during the build. The version declared with these options is automatically activated (if available installed). This is implemented with the [asdf](https://asdf-vm.com/) project.
2. Additional versions can be installed at runtime with a single command like `asdf install ruby 3.2.0`
3. Some Bitrise steps that depend on a tool - such as the Cocoapods or Fastlane steps - install the declared version automatically (if not available)

### How to declare tool versions
The best way to declare the specific tool version is via version files like `.ruby-version`, `.node-version`, `.tool-versions`, etc. By storing this information in the project repository, every developer's local environment can match the CI environment by using a version manager (we recommend [asdf](https://asdf-vm.com/), which handles the most common tools in one version manager).

The following version files are automatically recognized in the latest Ubuntu stack, as well as all macOS stacks:

- `.tool-versions` ([learn more](https://asdf-vm.com/manage/configuration.html#tool-versions))
- `.ruby-version`
- `.node-version`
- `.nvmrc`
- `.go-version`

On both Linux and macOS, the global `.tool-versions` file exists in the home directory. This defines the global tool defaults that can be overridden by placing a local version of the file in the root of the repository. Commands executed in the repository's directory or its subfolders will see the declared tool version in `$PATH`.

{{< hint warning >}}
Please note that the Ubuntu 20 stack doesn't enable asdf's `legacy_version_file` configuration option which means that it doesn't read `.ruby-version`, `.node-version`, `.nvmrc`, and `.go-version` files. We strongly recommend using the [Ubuntu 22 stack](https://stacks.bitrise.io/announcements/ubuntu-22/) instead.
{{< /hint >}}

Changing a version at runtime is also possible via the asdf CLI tool, for example:

```sh
asdf local ruby 3.2
asdf local nodejs 18.16
```

### asdf plugins

If an installed runtime is managed via asdf on our stacks, its corresponding plugin is also installed. The following runtime plugins are available on the different stacks:

* Ubuntu 20: Python, Ruby, Node.js
* Ubuntu 22: Python, Ruby, Node.js, Go, Flutter
* macOS: Ruby, Node.js, Go

In addition, the [asdf alias plugin](https://github.com/andrewthauer/asdf-alias) is installed on all stacks. 

### Version aliases
Not every possible tool version is preinstalled on the stacks, but there are special alias versions defined for every `major` and `major.minor` version. These aliases always point to the latest installed patch version and can be used like full version numbers.
For example, declaring Ruby `3.2` selects one preinstalled Ruby version, the latest available patch version of `3.2.x`.

{{< hint warning >}}
Because patch versions are sometimes upgraded (replaced in-place) on Bitrise stacks for critical bugfixes, we recommend declaring one of the alias versions (`major` or `major.minor`) in your project.
The implementation of version aliases is based on the [asdf alias plugin](https://github.com/andrewthauer/asdf-alias), which you can set up in the local environment too.
{{< /hint >}}

### Debugging version selection issues
To see what are the currently selected tool versions and why, run `asdf current` in a script step:

```
golang          1.20            /Users/vagrant/.tool-versions
nodejs          18              /Users/vagrant/workspace/.node-version
ruby            3.2             /Users/vagrant/.tool-versions
```
This shows that Go and Ruby versions are coming from the global `.tool-versions` file in the user home, while the Node.js version is coming from the current folder's `.node-version` file.
