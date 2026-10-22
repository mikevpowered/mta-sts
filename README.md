# MTA-STS policy for defenceactivated.com

This repository publishes one file, `.well-known/mta-sts.txt`, at https://mta-sts.defenceactivated.com/.well-known/mta-sts.txt through GitHub Pages.

MTA-STS tells other mail servers to deliver email for defenceactivated.com only over an encrypted connection to Google Workspace. It works with two DNS records at Wix: `_mta-sts` (TXT, the policy id) and `_smtp._tls` (TXT, where failure reports go).

- `.nojekyll` makes Pages publish the `.well-known` folder.
- After changing the policy, also change the id in the `_mta-sts` TXT record.
- Started in `mode: testing` on 22 Oct 2026. Move to `enforce` after about two weeks of clean TLS reports.
