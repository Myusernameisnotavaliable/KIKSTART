# Security policy

KIKSTART is an actively developed browser game. Security reports are welcome.

## Reporting a vulnerability

Please do not post suspected vulnerabilities, working credentials, personal information, or exploit details in a public issue, discussion, or pull request.

Use GitHub's **Private vulnerability reporting** feature for this repository if it is enabled. If that feature is unavailable, contact the repository maintainer privately through their GitHub profile and ask for a secure reporting channel. Do not include passwords, API keys, access tokens, or other live secrets in the initial report.

A useful report includes:

- A short description of the issue and its impact.
- The affected file, feature, or version, if known.
- Clear reproduction steps that do not expose other people's data.
- Any suggested mitigation.

Please allow the maintainer time to investigate and prepare a fix before publicly disclosing a vulnerability.

## Secrets and credentials

Never put personal access tokens, API keys, account passwords, private keys, or account-specific TURN credentials in browser-side source code, HTML, JavaScript, text assets, commits, or public issue reports. Anything shipped to a browser can be inspected by users.

If a real credential is accidentally committed, removing it from the latest file is not enough: revoke or rotate it with the service provider, then review the Git history and arrange history cleanup where necessary.
