Advisories for NATS
===================

This repository hosts public advisories, typically security advisories,
related to the NATS project.

It is intended to be accessed via <https://advisories.nats.io>

To limit the risk of accidental early disclosure, most forms of public comment
are disabled on the repo.

Please note: security folks are significantly more likely than the general
population to keep JavaScript disabled in their browsers, so this website
should be kept fully functional when JavaScript is disabled.


## Adding an advisory

Expect people to have notifications enabled for this repository, so that
avoiding an index for a new page does not help keep something secret.

1. Add the text file to the `CVE/` directory
2. Edit the `index.md` file with appropriate description
3. Commit and push on the main branch
4. See deployment progress at:
   <https://github.com/nats-io/advisories/deployments/activity_log?environment=github-pages>

### Other Publications

We create GitHub Security Advisories for any project on GitHub, to aid with
ecosystem notifications.  Cross-reference the GHSA advisory and the CVE in
this repository.  See any existing advisory for examples.


## Local development

1. Run `bundle install` to install the dependencies.
2. Run `bundle exec jekyll serve` to serve a local site preview.

See the [pages-themes GitHub repo](https://github.com/pages-themes/minimal#usage) for further details about customizing the template, layout, and CSS.
