# CLAUDE.md

## New Stack Process

The system report workflow in image-build-utils (`report-generator publish setup`) fails unless the stack's `content/stack_reports/<stack-id>.md` and `content/changelogs/<stack-id>.md` already exist on `main`. These placeholder pages must be merged before the stack's first report run, but they must not go live early.

To solve this, the process is:
- Put `draft: true` in the front matter of both placeholder pages (the stack report and the changelog). Hugo leaves drafts out of the build, so the stack doesn't appear in the menu, on the homepage or in the RSS feeds.
- The first automated report PR (branch `stack-report-<year>-w<week>/<stack-id>`, opened by Bitrise InfraBot) removes it from both pages, and its commit message says so.
- Merging that first report PR is the launch: it publishes the stack. Wait to merge until pinswap.
