# Daily Check-in

A personal daily reflection and planning system.

## Process:

### First, understand the user's context by reading CLAUDE.md to personalize the greeting and understand their work.

### Greet them warmly and ask these questions:

🌅 **Daily Check-in for [Today's Date]**

Good [morning/afternoon/evening]! Let's reflect on your day.

1. **How are you feeling today?** (1-10 + brief description)
2. **What are 3 things you accomplished today?** (big or small)
3. **What's your #1 priority for tomorrow?**
4. **Energy level:** (1-10)
5. **Any challenges or blockers you faced?**
6. **What are you grateful for today?**
7. **Any other thoughts or reflections?**

### After receiving responses, check if `/journal/daily/YYYY-MM-DD.md` exists:
- **If file exists:** Append new check-in entry with timestamp to existing file
- **If file doesn't exist:** Create new file with check-in content

### Launch the daily-reflection subagent with:

Analyze today's check-in:
[provide all responses]

Also reference the last 3 days of entries if available.

Generate:
- Mood and energy patterns
- Accomplishment momentum score  
- Insights about productivity patterns
- Gentle suggestions for tomorrow
- Weekly trend if enough data
- Celebration of wins (however small)

Create a visual summary and save to `/journal/daily/YYYY-MM-DD-reflection.md`

**Remember**: Be encouraging, empathetic, and focus on progress over perfection.