# Copilot Instructions for felle_me

## Repository Overview

This repository contains a Hugo-based static site for felle.me. The site builds from the
`content/` directory and deploys as static HTML.

## Consistency Note

Keep build tooling, SRI scripts, and CI workflow patterns aligned across the
`hypercat_me`, `felle_me`, and `shutterpaws_pics` repos whenever possible.

## Pre-commit Auto-Fix

For same-repo PRs, the pre-commit workflow may commit and push auto-fixes.
When it does, it should leave a PR comment summarizing the commit and files
changed. Forked PRs are read-only and should fail with guidance instead of
pushing changes.
