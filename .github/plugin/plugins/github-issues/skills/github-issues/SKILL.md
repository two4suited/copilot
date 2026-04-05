---
name: github-issues
description: Create, triage, and manage GitHub issues using the GitHub CLI
tools:
  - run_in_terminal
  - read_file
  - view
---

## Instructions

When asked to manage GitHub issues:

### Prerequisites
- Ensure `gh` CLI is installed and authenticated: `gh auth status`

### Creating Issues
- Create an issue: `gh issue create --title "Title" --body "Description"`
- Create with labels: `gh issue create --title "Title" --body "Body" --label "bug,priority:high"`
- Create with assignee: `gh issue create --title "Title" --body "Body" --assignee "@me"`
- Create with milestone: `gh issue create --title "Title" --body "Body" --milestone "v1.0"`

### Listing and Searching
- List open issues: `gh issue list`
- Filter by label: `gh issue list --label "bug"`
- Filter by assignee: `gh issue list --assignee "@me"`
- Filter by milestone: `gh issue list --milestone "v1.0"`
- Search issues: `gh issue list --search "query"`

### Managing Issues
- View issue details: `gh issue view <number>`
- Edit an issue: `gh issue edit <number> --title "New Title" --body "New Body"`
- Add labels: `gh issue edit <number> --add-label "enhancement"`
- Remove labels: `gh issue edit <number> --remove-label "bug"`
- Assign: `gh issue edit <number> --add-assignee "username"`
- Close an issue: `gh issue close <number>`
- Reopen: `gh issue reopen <number>`
- Add a comment: `gh issue comment <number> --body "Comment text"`

### Triage Workflow
When triaging issues:
1. List unlabeled issues: `gh issue list --search "no:label"`
2. Review each issue with `gh issue view <number>`
3. Apply appropriate labels, priority, and milestone
4. Assign to the right team member
5. Add a triage comment summarizing the assessment
