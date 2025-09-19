# Newsletter Researcher Command

## Purpose
Run a complete research → draft workflow for weekly newsletters.

## Steps
1. Read newsletter URLs from `Claude-DA/inputs/newsletter_links.md`  
   - If the file doesn’t exist, ask the user to provide links.  
   - Include Robert’s own newsletter and competitor newsletters.

2. Fetch recent posts from those URLs.  
   - Collect titles, dates, and links.  
   - Deduplicate by URL/title.  

3. Spawn subagent: `content-researcher`  
   - Task: Analyze sources, find trends, gaps, and time-sensitive angles.  
   - Save results as research report in `Claude-DA/metrics/research-YYYY-MM-DD.md`.

4. Spawn subagent: `newsletter-writer`  
   - Provide it the research report + `Claude-DA/rr_style_primer.md`.  
   - Task: Write subject lines and a complete 500–800 word draft in Robert’s voice.  
   - Include practical takeaways + natural, soft CTA.  
   - Save output in `Claude-DA/newsletter/drafts/newsletter-YYYY-MM-DD.md`.

## Output
- Research report file path (`/metrics/…`)  
- Draft file path (`/newsletter/drafts/…`)  

## Quality
- Voice matches Robert’s existing newsletters.  
- Draft is ready-to-send, not just an outline.  
- Value-first, authentic tone (avoid “AI-y” phrasing).  