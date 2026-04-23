# {{project-name}}

## Identity

{{one to three lines: who owns this project, what kind of work it supports, and the rules that always apply. Example: "This workspace is where I write, schedule, and archive my weekly newsletter. House style: plain prose, no fluff. Voice: mine, not corporate."}}

## Workspaces

- `{{workspace-1}}/`: {{one-line description of the mode of work}}
- `{{workspace-2}}/`: {{one-line description}}
- `{{workspace-3}}/`: {{one-line description}}

## Routing table

| Task | Go to | Read | Skills |
|------|-------|------|--------|
| {{task name}} | `{{workspace}}/` | `{{file1}}`, `{{file2}}` | {{skill-name or (none)}} |
| {{task name}} | `{{workspace}}/` | `{{file1}}` | (none) |
| {{task name}} | `{{workspace}}/` | `{{file1}}`, `{{file2}}` | {{skill-name}} |

## Naming conventions

Declare the patterns this project uses. Claude resolves "pull my demo v2" by convention when these are stated explicitly.

- Drafts: `{{topic}}_draft.md`
- Final: `{{topic}}_final.md`
- Dated output: `YYYY-MM-DD-{{slug}}.md`
- Versioned files: `{{name}}_v{{N}}.md`

## Rules

- Never reference one workspace's content inside another workspace's session.
- Do not rename a workspace folder once it exists. If a name must change, leave a redirect stub in the old folder.
- Sources in `{{raw-folder}}/` are the user's. Do not edit them.
- Keep this file under 50 lines. Every line is re-loaded on every prompt.
