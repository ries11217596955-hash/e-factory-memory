# MEMORY UPDATE — SITE_AUDITOR_AGENT

Status: ACTIVE BASELINE  
Line: SITE_AUDITOR_AGENT  
Date: 2026-03-16

## Summary
A new agent line is established: **SITE_AUDITOR_AGENT**.  
Purpose: one-repo site audit agent for Windows PC without admin rights.

## Scope
Current baseline v1 capabilities:
- reads a single target repo
- authenticates with GitHub token
- downloads repo snapshot
- builds inventory
- runs basic semantic audit
- emits ZIP audit pack into local outbox

Current non-goals / not yet baseline:
- live crawl of deployed site
- full navigation graph
- deep Eleventy render analysis
- auto-fix / auto-commit
- watcher / loop mode

## Delivery / Install Contract
Confirmed standard:
1. deliver agent as ZIP package
2. extract to local folder
3. place token/config
4. run `CREATE_SHORTCUT.ps1`
5. start via desktop shortcut

## Runtime Contract
- root resolver: use `$PSScriptRoot` as primary runtime root
- output location: `outbox` relative to agent root
- debug mode: do not diagnose launchers by double-click; use visible console

## Boundaries
SITE_AUDITOR_AGENT is NOT:
- mini-agent GitHub batch runner
- LM-agent / watcher / loop line

## Repo Mapping
- target site repo: `automation-kb`
- agent source repo target: `e-factory-agent`
- memory registration target: `e-factory-memory`
