---
title: Ruby 2.x deprecation
platform: [macOS, linux]
---

On Monday, June 26, 2023, Bitrise will remove all end-of-life Ruby versions from all Bitrise stacks. As a result, all apps using Ruby versions below 3.0 need to migrate to a newer version of Ruby.

**Why are doing this?**
All Ruby versions before 3.0 have reached their end of life and will no longer be supported. Therefore, we are now removing these to maintain security standards and to support more recent versions of Ruby as they are released.

**How will this impact you?**
If your applications are leveraging Ruby 2.7 or lower, you will need to transition to Ruby 3.0 or higher.

Ruby versions to be removed:
* 2.7.6 (current default)
* 2.7.5
* 2.7.2
* 2.6.9

Here is a guide on [Ruby versions on Bitrse](https://devcenter.bitrise.io/en/infrastructure/build-stacks/ruby-versions-on-bitrise.html)

**Timeline**
Incremental changes will be made with this deprecation to minimize the impact on existing builds and provide sufficient time to transition to Ruby 3.0 or higher.

* Monday, June 12, 2023, the default version of Ruby will change from 2.7.6 to 3.2.x
* Monday, June 26, 2023, all versions of Ruby lower than 3.0 will be removed.

**Actions you need to take**
Transition to Ruby version 3.0 or higher before Monday, June 26, 2023. If you still require versions of Ruby lower than 3.0, a custom script can be written to install it during your builds.

**Date by which you need to migrate**
Please ensure that you transition to Ruby version 3.0 or higher before Monday, June 26, 2023.

If you have any questions, please submit them via our [support page](https://support.bitrise.io/hc/en-us/requests).
