# AI Presentation Master (AI 簡報大師)

[繁體中文](README.md) · **English**

<p align="center">
  <a href="docs/ai-presentation-master-intro.mp4"><img src="docs/ai-presentation-master-intro.webp" alt="AI 簡報大師 intro" width="800"></a>
</p>
<p align="center"><sub>Click for the full video with music (MP4, 33s)</sub></p>

**AI can generate a beautiful deck in one click. Then your boss interrupts halfway: "So what's the conclusion?"**

AI Presentation Master (Chinese name: AI 簡報大師) is a skill that shows you how to **use AI tools to design a complete presentation, from idea to stage**: shaping your argument, structuring it, turning bullet lists into diagrams, setting layout and color, handing specs to tools like Gamma or Canva, and preparing your script, Q&A and final delivery checks — the whole deck, end to end.

The split is simple: **you set the direction, AI tools build it out.** The point of view and judgment are yours; AI does the making.

It uses the standard `SKILL.md` format and works with Claude Code, Codex, Gemini CLI, Cursor and other tools that support agent skills.

> **Language note:** the skill's content (`SKILL.md` and `references/`) is written in Traditional Chinese. It is designed for Chinese-speaking users; the agent will still follow it if you talk to it in English, but examples and prompt templates are in Chinese.

---

## Same request, two approaches

> "Next Wednesday I'm pitching our general manager for a NT$5M budget to adopt an AI customer-service system. About 20 minutes."

**Ask an AI to just make it:** you instantly get a 20-slide outline whose first slide says "In this rapidly changing era, AI is an irreversible trend." It looks complete, but none of it is your point of view, and nobody did the math on time.

**With AI Presentation Master:**

1. **It asks three questions first:** How much time do you have? What kind of setting is this? Will you present it live, or will people read it on their own?
2. **It turns time into content budget:** 20 minutes minus Q&A leaves roughly 15 minutes of talking; an audience retains at most about 3 core messages, so you land at roughly 12–20 slides. Slide count is calculated, not guessed.
3. **It picks the right structure:** when asking an executive for a decision, lead with the conclusion (Pyramid Principle) — don't build up background and reveal the ask at the very end.
4. **It draws out what only you know:** your viewpoint and real cases come from you. It helps you surface and organize them; it doesn't invent them.
5. **It prepares you for the hard questions:** the AI plays an ROI-focused CFO and runs through the toughest questions before you're on stage.

The difference isn't whether the slides look good. It's whether **you know what you're trying to convince them of** when you walk in.

---

## Stuck on one of these?

| What's happening | How it helps |
|---|---|
| Your manager cuts in: "So what's the conclusion?" | Switch to a conclusion-first structure; slide one states the decision you need |
| 32 slides, and your time just got cut in half | Cut evidence, not structure: drop from 3 messages to 2 and keep only the strongest example for each — don't just talk faster |
| A slide full of bullet points looks dull | First identify the relationship behind the bullets (sequence, composition, contrast, cause, overlap), then choose a step bar, quadrant or arrow chain |
| 40 carefully designed slides that still feel messy together | Set layout templates, align to a grid, unify icons and colors, plan the visual rhythm of the whole deck |
| The text sounds hollow, like AI wrote it | Point out the specific "AI tells" and rewrite with word limits and a banned-phrase list |
| You handed it to Gamma and the emphasis disappeared | Write a slide spec card — where the focus is, what the proportions are, what's forbidden — then translate it into instructions the tool follows |
| Sending it to a client and worried the fonts will break | Confirm the venue's aspect ratio and verify font embedding with `pdffonts` instead of trusting your own screen |
| Afraid the CFO will grill you | Anticipate tough questions, recognize questioner types, practice a four-step on-stage answer |
| You need to teach colleagues a 3-hour AI workshop | Plan with a module timetable instead of a slide count, cap lecture time, and design practice with feedback |

---

## Before and after

**Original**

> In this rapidly changing era full of challenges and opportunities, adopting AI customer service is an irreversible trend. Let's join hands to create a better future together.

**Problems:** stacked adjectives, no concrete information, and the audience doesn't know what to do afterward.

**Rewrite direction** (illustrative — replace the placeholders with your own real data)

> Night-shift complaints currently wait an average of [X] hours for a reply. AI customer service can handle [Y]% of common questions first — that's why I'm here today asking for this budget.

It will ask you for real numbers. It won't make one up and put it on your slide.

---

## You're the director; AI is the effects team

The full process has 13 steps, each labeled by who leads: you own the point of view, audience judgment and delivery; AI drafts layouts and charts first, and you review.

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontSize':'14px','lineColor':'#8A94A6'},'flowchart':{'nodeSpacing':18,'rankSpacing':30}}}%%
flowchart TB
    subgraph T["Think it through"]
        direction LR
        S1("1 Define the task") --> S2("2 Analyze audience") --> S3("3 Gather material") --> S4("4 Distill insight") --> S5("5 Design structure")
    end
    subgraph M["Build it"]
        direction LR
        S6("6 Plan slides") --> S7("7 First draft") --> S8("8 Polish") --> S9("9 Stress-test") --> S10("10 Layout") --> S11("11 Visualize")
    end
    subgraph D["Deliver it"]
        direction LR
        S12("12 Script & rehearse") --> S13("13 Ship the files")
    end
    T --> M --> D

    classDef human fill:#1F3A5F,stroke:#1F3A5F,color:#FFFFFF
    classDef co fill:#DCE6F2,stroke:#7E9CC0,color:#14213D
    classDef ai fill:#FFFFFF,stroke:#9AA5B1,color:#14213D
    class S1,S2,S12 human
    class S3,S4,S5,S8,S9,S13 co
    class S6,S7,S10,S11 ai
```

<sub>Dark: speaker leads · Light blue: co-created · White: AI drafts, speaker reviews</sub>

It covers four settings, each with its own success criteria and reading path: **business pitches, internal reports, public talks, and training sessions.** The same question can have opposite answers depending on the setting — information density, for example, should be low for a live talk and can be high for a deck people read on their own.

---

## What it doesn't do

- **It doesn't generate slide files in one click.** Once you've thought it through, build it in Gamma, Canva, open-slide or whatever you use; it helps you write the spec in a form those tools follow.
- **It doesn't invent cases or numbers.** Persuasion comes from real experience. Ask it to "make up a case" and it will first ask whether you have a real one to use.
- **It doesn't replace rehearsal.** Eye contact, pauses and reading the room can't be practiced by chatting with an AI. It will remind you to run it once in front of a real person.

---

## Install

Put the folder in your agent's skills directory. For Claude Code:

```bash
git clone https://github.com/chengwesley/ai-presentation-master ~/.claude/skills/ai-presentation-master
```

## Try one of these first

- "I have a 15-minute talk — how many slides should I make?"
- "I'm pitching a client next week and I'm worried about tough questions. How do I prepare?"
- "This slide lists five items and looks boring. Can it become a diagram?"

---

## Files

```
ai-presentation-master/
├── SKILL.md            # Entry point: process, scenario routing, principles
├── references/         # 14 topic files, loaded on demand by scenario or symptom
└── evals/              # 9 scenario test cases + 20 trigger tests
```

## License

[MIT](LICENSE)
