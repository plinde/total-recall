# RECALL INCORPORATED
## Memory Preservation Services for Claude Code Sessions

> **Quaid:** "Where am I?"
>
> **Johnnycab:** "You're in a Johnnycab."
>
> **Quaid:** "I mean, what am I doing here?"
>
> **Johnnycab:** "I'm sorry. Would you please rephrase the question?"
>

![Johnnycab](images/total-recall-how-did-i-get-here.gif)

Ever feel like Douglas Quaid after hitting `Context left until auto-compact: 0%`? Returning to a Claude Code session nearly devoid of context, with no idea who you are or what you've been doing? The final insult is delivered by Claude helpfully informing you that "You're in a Claude session", just like Johnnycab?

**Welcome to Recall Inc.** - Your trusted provider of professional memory preservation services. When you need to maintain context across Claude Code sessions, we're here to ensure nothing gets lost in the transition.

## Reality Check

**Step 1: Recognize the Early Warning Signs**

- Do you have too many tools loaded?
- Is your context window getting low?
- Have you deviated far your original plans?

If this sounds like you, Recall has the solution.

> "Let me suggest you take a vacation, from yourself"

![Hauser Message](images/quaid-turns-off-tv.gif)

You need to consider your context window utilization when:
- Claude Code conversations are getting too long (approaching token limits)
- You've been switching between multiple complex tasks over a long session
- You're about to resort to a preemptive `/compact` but can't afford to lose state

---

**Step 2: Activate Recall Services**

![Get to Mars](images/get-to-mars.gif)

```bash
# Invoke the total-recall skill
/total-recall
```

Claude will create a comprehensive memory dump at `/tmp/total-recall` containing:
- Your current work state
- All key decisions made during the session
- File paths and artifacts created
- Next steps and action items
- Important technical notes

---
**Step 3: Free Your Mind**

![Quaid Relaxed](images/quaid-relaxed.gif)

```bash
# Clear your session
/reset
```

Your conversation history is cleared, but your critical context is safe in `/tmp/total-recall`.

---
**Step 4: Restore Your Memory**

![Get to Mars](images/hauser-message.gif)  

```
User: read /tmp/total-recall to resume

Claude: I'm now up to speed on your AWS account inventory project.
        You were working on the SQLite schema migration.
        Which task would you like to continue with?
```

## Total Preservation (Almost) Guaranteed or Your Money Back

The total-recall skill captures:

1. **Current State** - What you're working on
2. **Key Decisions Made** - Important choices and rationale
3. **Data/Inventory Summary** - Project-specific information
4. **Generated Files/Artifacts** - Paths to created files
5. **Next Steps** - Clear action items (with ✅ completion status)
6. **Important Notes** - Constraints and technical details

## Need to clear out bad context?

![Removing Implant](images/quaid-removing-implant.gif)

Sometimes you just need to rip out the bad memories and start fresh with `/reset`.

## Installation & Setup

Clone the repository and create symlinks:

```bash
CLONE_DIR="wherever-you-like"
git clone https://github.com/plinde/total-recall ${CLONE_DIR}
ln -s ${CLONE_DIR} ~/.claude/skills/total-recall
ln -s ${CLONE_DIR}/COMMAND.md ~/.claude/commands/total-recall.md
```

That's it! Now you can use:

```
User: /total-recall
```

This invokes the total-recall skill and saves to `/tmp/total-recall`.

## Optional: Automatic Context Preservation

For automatic preservation before context compaction, add a PreCompact hook to `~/.claude/settings.json`:

```json
{
  "hooks": {
    "PreCompact": [
      {
        "hooks": [
          {
            "type": "prompt",
            "prompt": "Context compaction is about to occur. Use the total-recall skill to preserve the current session context before compaction. This is critical - invoke /total-recall now to save session state."
          }
        ]
      }
    ]
  }
}
```

This automatically triggers total-recall right before Claude compacts your context, ensuring nothing is lost during compaction.

**See [hooks-example.json](hooks-example.json) for a complete example.**

## License

MIT License - See [LICENSE](LICENSE)

## Acknowledgments

- The `total-recall` skill - The real hero
- Paul Verhoeven - For the greatest sci-fi action film ever made (1990)
- Arnold Schwarzenegger - For the memorable one-liners
- Philip K. Dick - Original author of "We Can Remember It for You Wholesale"

---

> "Get your ass to Mars" - Hauser
