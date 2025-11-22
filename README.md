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
> **Quaid:** "How did I get in this taxi?"
>
> **Johnnycab:** "The door opened. You got in."
>
> *[Johnnycab rolls his eyes]*

![Johnnycab](images/johnnycab.jpg)

---

Ever feel like Douglas Quaid after hitting `Context left until auto-compact: 0%`? Returning to a Claude Code session nearly devoid of context, with no idea where you are or what you're doing? The final straw being delivered by Claude helpfully informing you that "You're in a Claude session", just like Johnnycab?

**Welcome to Recall Inc.** - Your trusted provider of professional memory preservation services. When you need to maintain context across Claude Code sessions, we're here to ensure nothing gets lost in the transition.

> "We can remember it for you wholesale."

---

## Reality Check

![Hauser Message](images/hauser-message.gif)

**Step 1: Recognize the Warning Signs**

![Get to Mars](images/get-to-mars.gif)

You need context preservation when:
- Claude Code conversations are getting long (approaching token limits)
- You're switching between multiple complex tasks
- You need to clear history but can't afford to lose state
- You're about to use `/compact` or `/reset`

**Step 2: Activate Recall Services**

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

**Step 3: Free Your Mind**

![I Give Up](images/i-give-up.gif)

```bash
# Clear your session
/reset
```

Your conversation history is cleared, but your critical context is safe in `/tmp/total-recall`.

**Step 4: Restore Your Memory**

![Quaid Relaxed](images/quaid-relaxed.gif)

```
User: read /tmp/total-recall to resume

Claude: I'm now up to speed on your AWS account inventory project.
        You were working on the SQLite schema migration.
        Which task would you like to continue with?
```

### What Gets Preserved

The total-recall skill captures:

1. **Current State** - What you're working on
2. **Key Decisions Made** - Important choices and rationale
3. **Data/Inventory Summary** - Project-specific information
4. **Generated Files/Artifacts** - Paths to created files
5. **Next Steps** - Clear action items (with ✅ completion status)
6. **Important Notes** - Constraints and technical details

---

## When to Use Context Preservation

#### ✅ Use Recall Services When:
- Approaching token limits and need to `/compact` or `/reset`
- Working on complex, multi-step tasks with critical state
- Switching between different projects
- Building up conversation history debt

### Need to Clear Bad Context?

![Removing Implant](images/quaid-removing-implant.gif)

Sometimes you just need to rip out the bad memories and start fresh with `/reset`.

---

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

---

## License

MIT License - See [LICENSE](LICENSE)

---

## Acknowledgments

- The `total-recall` skill - The real hero
- Paul Verhoeven - For the greatest sci-fi action film ever made (1990)
- Arnold Schwarzenegger - For the memorable one-liners
- Philip K. Dick - Original author of "We Can Remember It for You Wholesale"

---

> "See you at the party, Richter!"
