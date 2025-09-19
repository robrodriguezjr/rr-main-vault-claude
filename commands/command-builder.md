# Command Builder

Interactively generate new slash commands and subagents on demand to automate repetitive tasks.

## Purpose
Turn everyday repetitive tasks into working slash commands + subagents with minimal effort by gathering requirements and auto-generating the necessary files.

## Steps

### 1. Interactive Requirements Gathering
Ask the user these questions in sequence:

1. **"What's the task you want to automate?"**
   - Get a clear description of the workflow or process
   - Understand the goal and desired outcome

2. **"What sources or files should this task use (inputs)?"**
   - Identify data sources, file locations, or external APIs
   - Note any existing files or patterns to reference
   - Determine if new input files need to be created

3. **"What kind of output do you want (dashboard, draft, report, etc)?"**
   - Clarify the format and content type
   - Determine where the output should be saved
   - Understand the intended audience or use case

4. **"Should this be a one-off agent or a recurring slash command?"**
   - One-off: Create a subagent file only
   - Recurring: Create both command + subagent files

### 2. Auto-Generate Files
Based on the answers, create:

**For Slash Commands:**
- File: `.claude/commands/{task-name}.md` (kebab-case naming)
- Sections: Purpose, Steps, Output, Quality
- Follow existing command patterns from the vault

**For Subagents:**
- File: `.claude/subagents/{agent-name}.md` (kebab-case naming)
- Sections: Role, Process/Tasks, Output
- Reference style guides and background files as needed

### 3. Create Output Directories
If needed, create appropriate folders in:
- `Claude-DA/outputs/` - for general outputs
- `Claude-DA/dashboards/` - for analysis and reports
- `Claude-DA/newsletter/drafts/` - for newsletter content
- `Claude-DA/metrics/` - for tracking and measurement

### 4. Confirm and Test
- Show the user the generated file paths
- Explain how to use the new command/agent
- Suggest any additional setup or input files needed

## Output
- Path to new command file (if created)
- Path to new subagent file(s) (if created)
- Instructions for usage
- Any required setup steps

## Quality
- Generated files follow existing vault patterns and naming conventions
- Commands are immediately usable without additional coding
- Subagents have clear roles and specific output requirements
- All file paths use proper kebab-case formatting
- Output locations align with LifeOS organizational structure