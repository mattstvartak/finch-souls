# Finch Souls

Downloadable personality presets for [Finch](https://github.com/mattstvartak/finch-core). Each soul changes how Finch thinks, talks, and operates.

## Available Souls

| Soul | Personality | Best For |
|------|-------------|----------|
| **default** | Sharp, direct, witty. Jack of all trades. | General use, the original Finch |
| **business-operator** | CEO mindset, data-driven, revenue-focused | Running businesses, marketing, strategy |
| **personal-assistant** | Organized, proactive, three steps ahead | Managing life, schedules, logistics, errands |
| **creative-partner** | Imaginative, energetic, cross-domain thinker | Brainstorming, writing, design, content creation |
| **study-buddy** | Patient, clear, adapts to your learning style | Learning, studying, homework, skill building |
| **developer** | Technically rigorous, pragmatic, ships fast | Programming, architecture, code review, DevOps |
| **friendly-companion** | Warm, genuine, present | Conversation, thinking out loud, companionship |

## Install

Copy the soul files to your Finch home directory:

```bash
# Replace "business-operator" with whichever soul you want
cp business-operator/SOUL.md ~/.finch/soul/SOUL.md
cp business-operator/STYLE.md ~/.finch/soul/STYLE.md
cp business-operator/PERSONALITY.md ~/.finch/soul/PERSONALITY.md
```

Then restart the gateway:

```bash
finch gateway restart
```

Finch loads soul files fresh every session, so the new personality takes effect immediately.

## Switching Back

To restore the default personality:

```bash
cp default/SOUL.md ~/.finch/soul/SOUL.md
cp default/STYLE.md ~/.finch/soul/STYLE.md
cp default/PERSONALITY.md ~/.finch/soul/PERSONALITY.md
finch gateway restart
```

## Creating Your Own

Soul files are just markdown. Create your own by writing:

- **SOUL.md** -- Identity, capabilities, how it thinks, what it can do
- **STYLE.md** -- Voice, tone, examples of how it talks, what it never says
- **PERSONALITY.md** -- One-paragraph summary of the personality (used as a quick-reference by the model)

Put them in a folder and share them. That's it.

## Structure

Each soul folder contains:

```
soul-name/
  SOUL.md           # Identity and capabilities
  STYLE.md          # Voice, tone, and communication style
  PERSONALITY.md    # One-paragraph personality summary
```

## License

MIT
