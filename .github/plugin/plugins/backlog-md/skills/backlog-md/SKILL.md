---
name: backlog-md
description: Manage project tasks using Backlog.md - a markdown-native task manager with CLI and MCP support
tools:
  - run_in_terminal
  - create
  - view
---

## Instructions

When asked to manage project tasks, backlogs, or Kanban boards using Backlog.md:

### Initialization
1. Check if Backlog.md is installed: `which backlog`
2. If not installed, install with: `npm i -g backlog.md`
3. Initialize in the current repo: `backlog init "Project Name"`
4. Choose MCP connector when prompted for AI integration

### Task Management
- Create a task: `backlog task create "Title" -d "Description" --ac "Acceptance criteria"`
- List tasks: `backlog task list`
- Filter by status: `backlog task list -s "To Do"`
- Edit a task: `backlog task edit BACK-<id> -d "Updated description"`
- Search tasks: `backlog search "query"`

### Visualization
- Terminal Kanban board: `backlog board`
- Export board: `backlog board export`
- Web interface: `backlog browser`

### MCP Integration
Backlog.md provides an MCP server for direct agent integration:
```json
{
  "mcpServers": {
    "backlog": {
      "command": "backlog",
      "args": ["mcp", "start"]
    }
  }
}
```

### Workflow
Follow the spec-driven AI development approach:
1. Decompose work into small tasks with clear descriptions and acceptance criteria
2. Work on one task at a time, one PR per task
3. Research and write an implementation plan before coding
4. Implement, verify, and close the task
