# Documentation rules

**English** | [Deutsch — canonical](domain.de.md)

## Entry points and storage

Read `README.md`, `profile/README.de.md`, and `profile/README.md` first. This repository contains the public organization profile. Maintain changes to claims and principles in both profile languages. Product research and architecture decisions belong in their respective repositories. Include private development content in the public profile only when explicitly requested for publication.

## Context and decisions

Treat each repository as one context. If `CONTEXT.md` exists, read it before domain work and use its terminology. Existing documentation remains the entry point when that file is absent. Do not create an extra context map or parallel ADR directory solely for skill setup.

Read relevant existing decisions before making changes. Explicitly identify conflicts with sources and rationale rather than silently overriding decisions. Distinguish research findings, candidates, and accepted architecture. Prefer links to authoritative documents over duplicating their contents as a second source of truth.

## Repository responsibilities

`product-development` records questions, experiments, and findings. `architecture` contains supported architecture and ADRs. `.github` contains the public presentation. Configuration in one repository does not automatically apply to others; each receives its own configuration.
