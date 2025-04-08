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

We use GitHub's ability to request a CVE as part of drafting a
GitHub Security Advisory (GHSA).
Getting a CVE through the formerly used process has become not expeditious.

Even if we request a CVE via another means, the GHSA should still be created;
this helps with ecosystem notifications.

Cross-reference the GHSA advisory and the CVE in this repository.

Go to the repository's "Security" tab, "Security advisories" section.  
Eg: <https://github.com/nats-io/nats-server/security/advisories>.  
You can and should draft an advisory ahead of time; publishing the advisory is
almost irreversible.  (It can still be edited, but can't be made private
again).

### Other Publications

For software which can be used as a Go library, we file an issue to update the
Go Vulnerability Database, when we go public.  See the next section.

### Publicising the Advisory

1. **Important**: `grep -r FIXME .`  
   Check that all FIXMEs have been resolved.
   Learn from Phil's mistakes.
   See the repo history on 2025-04-08 and help us not repeat this.
2. The push to the GitHub repo, on any branch, will alert people who have
   watches set up, so from that moment on the public clock is ticking.
3. Send a copy to the `oss-security` mailing-list, which is the main current
   announcement mailing-list for open source software security issues;
   <https://oss-security.openwall.org/wiki/mailing-lists/oss-security> /
   <https://www.openwall.com/lists/oss-security/>
4. GHSA: _if this is the same text as the advisory here_ (it normally is)
   then mark this public now.
   If the text differs, use discretion to establish a publication timeline.
   + Eg, secnote-2025-01 came from an external report with more detail than we
     wanted public on the day of announcement, but we didn't want to censor,
     so publication held back for one week.
5. For Go vulnerabilities, file an issue to update the
   [Go Vulnerability Database](https://go.dev/security/vuln/database) using
   [this ticket-opening shortcut](https://go.dev/s/vulndb-report-new), as
   [documented in the announcement blog-post](https://go.dev/blog/vuln).
6. Notify Slack in various places: natsio #general, gophers #nats
7. If really disastrous, consider getting a tweet tweeted from the official
   account.
8. (Update the official CVE registration details.) -- this should be handled
   by GitHub once the advisory is marked public.


## Local development

1. Run `bundle install` to install the dependencies.
2. Run `bundle exec jekyll serve` to serve a local site preview.

See the [pages-themes GitHub repo](https://github.com/pages-themes/minimal#usage) for further details about customizing the template, layout, and CSS.
