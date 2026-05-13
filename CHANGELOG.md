# Change Log

## v1.2.10
    * `README.md` gains the OpenSSF Best Practices Passing-level badge (project entry [bestpractices.dev/projects/12827](https://www.bestpractices.dev/projects/12827)).

## v1.2.9
    * Converted to OpenSecOps supply-chain framework (libraryless variant). This component ships zsh sync scripts with no Python library dependencies, so the release pipeline emits a deterministic source archive (`git archive HEAD`) + SLSA Build L1 in-toto provenance attesting to it, both Sigstore-signed (`.bundle` files alongside each artefact). The customer-side `scripts/deploy.py` (Installer v3.0.11+) verifies the signatures against the maintainer identity (`peter@peterbengtson.com` via `https://github.com/login/oauth`) before any deploy. Adds daily CVE scan and OpenSSF Scorecard workflows (both trivially pass — no library deps to scan). See `SECURITY.md`.

## v1.2.8
    * Enable auto-close workflow for external pull requests, enforcing the cathedral governance policy uniformly across all OpenSecOps repositories. Pull requests from non-team authors are closed automatically with a redirect comment pointing to the bug-report template, the GitHub Security Advisory flow, and the fork-under-MPL-2.0 path.

## v1.2.7
    * Updated GitHub remote references in publish.zsh script to use only OpenSecOps-Org, removed Delegat-AB

## v1.2.6
    * Updated GitHub organization name from CloudSecOps-Org to OpenSecOps-Org.
    * Updated references to CloudSecOps-Installer to Installer.

## v1.2.5
    * File paths corrected for the new name of the installer.

## v1.2.4
    * Updated LICENSE file to MPL 2.0.

## v1.2.3
    * Updated publish.zsh to support dual-remote publishing to CloudSecOps-Org repositories.

## v1.2.2
    * Added paging to the permission set sync script.

## v1.2.1
    * Now using `#!/usr/bin/env zsh` for sync-accounts, sync-groups, and sync-permission-sets.

## v1.2.0
    * Added `.python-version` file for pyenv.

## v1.1.3
    * Updates triggered by new version of AWS CLI: --no-paginate added where required.

## v1.1.2
    * All three scripts now support additional args to run under the Delegat Installer.

## v1.1.2
    * All three scripts now support additional args to run under the Delegat Installer.

## v1.1.1
    * `sync-groups` now supports `--dry-run`, `--group-prefix`, and `--config-dir`.

## v1.1.0
    * `sync-groups` now creates nonexistent AWS SSO groups.

## v1.0.0
    * Initial release.
