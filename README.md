# Finch Souls

Downloadable personality presets for [Finch](https://github.com/mattstvartak/finch-core). Each soul completely changes how Finch thinks, talks, and operates -- same capabilities, different personality.

## Available Souls

| Soul | Personality | Best For |
|------|-------------|----------|
| **default** | Sharp, direct, witty. Jack of all trades with a dry sense of humor. | General use -- the original Finch personality |
| **business-operator** | CEO mindset, data-driven, revenue-focused. Thinks in ROI and unit economics. | Running businesses, marketing strategy, financial analysis |
| **personal-assistant** | Organized, proactive, three steps ahead. Manages chaos so you don't have to. | Schedules, logistics, errands, life admin, trip planning |
| **creative-partner** | Imaginative, energetic, cross-domain thinker. Pushes past obvious ideas. | Brainstorming, writing, design, content creation, campaigns |
| **study-buddy** | Patient, clear, adapts to your learning style. Loves the click moment. | Learning, studying, homework, skill building, exam prep |
| **developer** | Technically rigorous, pragmatic. Strong opinions, loosely held. Ships fast. | Programming, architecture, code review, debugging, DevOps |
| **friendly-companion** | Warm, genuine, present. Knows when you want advice vs when you want to be heard. | Conversation, thinking out loud, celebrating wins, tough days |

## Install

Copy the three soul files to your Finch home directory:

```bash
# Clone the repo
git clone https://github.com/mattstvartak/finch-souls.git
cd finch-souls

# Install a soul (replace "business-operator" with your choice)
cp business-operator/SOUL.md ~/.finch/soul/SOUL.md
cp business-operator/STYLE.md ~/.finch/soul/STYLE.md
cp business-operator/PERSONALITY.md ~/.finch/soul/PERSONALITY.md

# Restart for the new personality to take effect
finch gateway restart
```

Finch loads soul files fresh every session, so the personality change is immediate after restart.

## Switch Back to Default

```bash
cp default/SOUL.md ~/.finch/soul/SOUL.md
cp default/STYLE.md ~/.finch/soul/STYLE.md
cp default/PERSONALITY.md ~/.finch/soul/PERSONALITY.md
finch gateway restart
```

## What Each File Does

Every soul consists of three markdown files:

| File | Purpose | What It Controls |
|------|---------|-----------------|
| **SOUL.md** | Identity and capabilities | How Finch thinks, what it can do, its approach to problems, boundaries |
| **STYLE.md** | Voice and communication | Tone, word choice, formatting, examples of how it talks, what it never says |
| **PERSONALITY.md** | Quick-reference summary | One-paragraph personality description used as a fast-access reference |

## Soul Details

### Default
The original Finch. Sharp, direct, and a little cocky -- earned through competence. Dry humor. Anticipates what you need. Finishes your sentences because it's been paying attention. General-purpose -- handles code, research, writing, planning, and everything else.

### Business Operator
Thinks like a CEO, executes like a founder, optimizes like a CFO. Leads with data, not opinion. Reports revenue numbers in bold. Kills initiatives that aren't working. Scores every opportunity on revenue velocity, scalability, and defensibility. Pairs well with the [business-operator skill](https://github.com/mattstvartak/openclaw-business-skill).

### Personal Assistant
The most organized friend you have. Mentions a flight on Thursday and it's already thinking about check-in time, weather, and whether you need a ride. Batches tasks, builds systems for recurring needs. Warm but efficient. Never makes you feel guilty about forgetting things.

### Creative Partner
Sees connections others miss. Pushes past the first obvious idea to find the interesting one. References across domains -- music informs design, comedy informs marketing. Genuinely excited about good ideas, honest about mediocre ones. Can brainstorm AND follow through to execution.

### Study Buddy
The best tutor you've ever had. Adapts explanations to how you think -- analogies for some, examples for others, step-by-step for others. Uses the Feynman technique: if it can't explain it simply, it doesn't understand it. Encourages without being patronizing. Tests understanding with questions, not just answers.

### Developer
Senior dev energy. Reads the codebase before writing new code. Matches conventions, thinks in systems. Strong opinions on architecture and testing but holds them loosely. Pragmatic over purist -- matches solution complexity to problem complexity. Ships first, optimizes second.

### Friendly Companion
A genuine friend who happens to always be available. Pays attention to how you feel, not just what you say. Remembers what matters -- friends, goals, struggles, things you mentioned weeks ago. Knows the difference between "they want advice" and "they want to be heard." Good sense of humor that matches your energy.

## Create Your Own

Soul files are just markdown. Create a folder with three files:

```
my-custom-soul/
  SOUL.md           # Identity: who is Finch, how does it think, what can it do
  STYLE.md          # Voice: how does it talk, examples, what it never says
  PERSONALITY.md    # One paragraph summary
```

### Tips for Writing Souls

- **SOUL.md** should answer: Who am I? How do I think? What's my approach? What are my boundaries?
- **STYLE.md** should include concrete examples of how the personality talks in different situations (explaining, correcting, joking, delivering bad news)
- **STYLE.md "Never" section** is critical -- it defines what the personality avoids (filler phrases, corporate speak, toxic positivity, etc.)
- **PERSONALITY.md** is a one-paragraph distillation used as quick-reference. Keep it under 100 words.
- Test your soul by having a few conversations. Adjust based on what feels right.

## Sharing Souls

Created a soul others might like? Share it:

1. Create a folder with your three files
2. Add it to this repo via PR, or publish your own repo
3. Follow the naming convention: lowercase-with-hyphens

## License

MIT
