# Bitrise Stacks

This repo contains the static site behind https://bitrise-io.github.io/stacks/.

### Useful links

- [Build stacks](https://devcenter.bitrise.io/en/infrastructure/build-stacks.html)
- [Stack update policy](https://devcenter.bitrise.io/en/infrastructure/build-stacks/stack-update-policy.html)

### Development

The raw data of stack reports is in the `data/stack-id` folders.

The rest is a [Hugo](https://gohugo.io/) site with some custom logic in `layouts/shortcodes`.

To generate the static site locally, run:

```
go install -tags extended github.com/gohugoio/hugo@latest

hugo serve

```

### JSON API

Next to the static HTML output, there is also a JSON output format for some content types. These JSON "endpoints" are based on [Hugo output templates](https://gohugo.io/templates/output-formats/#customizing-output-formats) and are defined in [themes/bitrise/layouts](/themes/bitrise/layouts) in the `single.json.json` and `list.json.json` files.
