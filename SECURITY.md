# Security policy

This policy applies to every `icyhoty2k` repository that does not carry one of its own.

## Reporting a vulnerability

**Email <icyhoty2k@gmail.com>.** Put "security" in the subject.

Please do **not** open a public issue for a security problem. An issue is visible the
moment it is filed, which tells everyone about the hole before there is a fix.

If GitHub's private vulnerability reporting is enabled on the repository, that works
too and is the tidier route: **Security → Report a vulnerability**.

## What to include

What you would want if you were fixing it:

- Which project, and which version. QuickImageViewer shows its version in the About
  box; qIV Remote on its About screen.
- What an attacker can do — reading files, crashing the app, running code, reaching the
  network.
- The steps to reproduce it. **A file that triggers the bug is worth more than any
  description of it**, and image decoders are the most likely place for one.
- Your operating system, and for the Android app the device and Android version.

## What happens next

This is one person working evenings, so honest expectations rather than a corporate
service level:

- I will acknowledge your report, usually within a few days.
- I will tell you whether I can reproduce it and whether I agree on the severity.
- Fixes for anything that lets an attacker run code or read files outside the opened
  file get priority over everything else, including features.
- I will credit you when the fix ships, unless you would rather I did not.

There is no bug bounty. I have no money to offer, and I would rather say so plainly
than imply otherwise.

## Scope

**In scope:** the applications themselves, the release binaries, and the code in these
repositories.

**Particularly welcome:** anything in the image decoders. They size buffers from values
in files that came from strangers, which is the classic shape of a memory-safety bug,
and it is the part I most want another pair of eyes on.

**Out of scope:** the GitHub Pages sites, which are static files with no server-side
code, no forms and no third-party scripts. Reports about missing security headers on a
static site are noted but not acted on.
