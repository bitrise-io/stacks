# Bitrise Stacks - test PR

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
