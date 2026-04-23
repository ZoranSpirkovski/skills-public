---
type: source
created: 2026-04-23
updated: 2026-04-23
sources: 1
tags: [foundation, three-layer, customization, examples]
---

# foundation-3-2-customizing-for-your-use-case

> Packaged inside `.wiki/raw/the-foundation.md`, lines ~1451-1688. Foundation Module 3, Lesson 2.

## Summary

The three-layer architecture from [[foundation-3-1-full-walkthrough]] reshapes for different kinds of work without changing the layers. Van Clief walks three concrete workspace blueprints: content creator (script-lab, production, distribution), freelancer/consultant (one folder per client, plus templates and business-dev), and developer (planning, src, docs, ops). Each comes with an example `CLAUDE.md` that shows the routing table and naming conventions. The layers stay the same; the labels, context files, and routing rules change. The closing section is the four-step build process: list workspaces, write a `CONTEXT.md` each, write the `CLAUDE.md` routing table, start working and iterate.

## Key claims

1. The three layers do not change across domains; only labels, context files, and routing rules do.
2. Content creator workspace set: Script Lab (ideas/drafts/final), Production (briefs/specs/builds/output), Distribution (platforms/scheduling/analytics).
3. Freelancer workspace set: one folder per active client plus shared Templates and Business-Dev folders; explicit rule that one client's information never enters another's workspace.
4. Developer workspace set: Planning (specs/architecture/decisions), Src (components/services/utils/tests), Docs (api/guides/changelog), Ops (deploy/monitoring/scripts). Developer example is the one that demonstrates the Skills column on the routing table.
5. Four-step build: list 2-4 workspaces by mental mode, draft a short `CONTEXT.md` per workspace, build the `CLAUDE.md` with routing table and naming conventions, start working and edit context files as understanding sharpens.
6. Workspace boundaries are detected by asking "do I shift mental modes between these tasks?" - not by surface-level topic differences.
7. Context files are living documents; the high-leverage habit is editing them as projects evolve.

## Entities mentioned

- [[van-clief]]

## Open questions

- The Production CLAUDE.md examples for each profile are referenced as being in The Vault (Premium); not available inline.
- The freelancer rule "never reference one client's information in another client's workspace" is a hard isolation claim that may need a lint check for the user's actual setups.
