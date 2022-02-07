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


## Adding an Advisory

Expect people to have notifications enabled for this repository, so that
avoiding an index for a new page does not help keep something secret.

1. Add the text file to the `CVE/` directory
2. Edit the `index.md` file with appropriate description
3. Commit and push on the main branch
4. See deployment progress at:
   <https://github.com/nats-io/advisories/deployments/activity_log?environment=github-pages>

### Getting a CVE assignment

CVEs are typically requested from MITRE as the CNA of last resort for open
source projects: <https://cveform.mitre.org/>

Fill out enough details to get the number; be accurate, or withhold data, as
appropriate.  At this first stage, I usually make sure to classify the type of
vulnerability and the affected version numbers, but not much more.

After the CVE has been published, we can update the text with another use of
this form.


### Other Publications

We create GitHub Security Advisories for any project on GitHub, to aid with
ecosystem notifications.  Cross-reference the GHSA advisory and the CVE in
this repository.  See any existing advisory for examples.

### Publicising the Advisory

1. The push to the GitHub repo, on any branch, will alert people who have
   watches set up, so from that moment on the public clock is ticking.
2. Send a copy to the `oss-security` mailing-list, which is the main current
   announcement mailing-list for open source software security issues;
   <https://oss-security.openwall.org/wiki/mailing-lists/oss-security> /
   <https://www.openwall.com/lists/oss-security/>
3. Create a GitHub security advisory; this will help downstream users get
   automatic notifications if they depend upon the affected software.
   The repository's "Security" tab, "Security advisories" section.  
   Eg: <https://github.com/nats-io/nats-server/security/advisories>.  
   You can draft an advisory ahead of time; publishing the advisory is almost
   irreversible.
4. Notify Slack in various places: natsio #general, gophers #nats
5. If really disastrous, consider getting a tweet tweeted from the official
   account.
6. Update the official CVE registration details.


## Local development

1. Run `bundle install` to install the dependencies.
2. Run `bundle exec jekyll serve` to serve a local site preview.

See the [pages-themes GitHub repo](https://github.com/pages-themes/minimal#usage) for further details about customizing the template, layout, and CSS.
