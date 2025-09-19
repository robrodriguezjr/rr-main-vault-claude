# Daily Brief

Create a personalized daily news briefing system that learns what I care about.

## Process:

### Analyze my files to identify my interests
- Read CLAUDE.md
- Launch interest-analyzer subagent to extract key topics I care about

### Use web search to find news from THE LAST 7 DAYS ONLY
- Search for stories related to my identified interests
- MUST include publication dates on all stories
- Only include stories from the past week
- Verify all dates before including

### Filter and curate content
- Launch news-curator subagent to:
  - Filter for relevance and actionability
  - Add context about why each item matters to me
  - Suggest actions I could take
  - Explain the significance

### Save briefing to `Claude-DA/dashboards/daily-brief-{{date}}.md`

**IMPORTANT**: Make sure all news is current and relevant. No outdated or fabricated stories.