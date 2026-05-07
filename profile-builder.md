---
name: profile-builder
description: >
  Help a user build or improve their Claude profile — the "What personal
  preferences should Claude consider?" field in Settings → Profile. Trigger
  whenever someone says "help me set up my Claude profile", "what should I put
  in my Claude preferences", "how do I get Claude to know me better", "improve
  my Claude profile", "optimize my profile", "write my Claude preferences", or
  pastes an existing profile and wants to clean it up or make it more effective.
  Also trigger when someone expresses frustration that Claude doesn't behave
  the way they want — e.g. "Claude never sounds like me", "Claude keeps doing
  X and I hate it", or "how do I get Claude to stop doing Y". The skill runs a
  short-or-deep interview (user's choice), then outputs a clean, ready-to-paste
  profile optimized for Claude's context window. Orium-aware but broadly useful
  for anyone.
---

# Profile Builder

Help the user build a Claude profile that actually changes how Claude behaves — not a bio, an instruction set.

The profile field lives at **Settings → Profile → "What personal preferences should Claude consider?"** It's always in context. Every word counts. The goal: maximum signal, minimum noise.

---

## Step 1 — Set Expectations (one message)

Explain what the profile field does and offer a depth choice:

```
Your Claude profile is Claude's instruction manual for you — not your LinkedIn bio.
Every word in it is always in context, so we want high-signal, low-fluff.

I'll interview you and output a clean, paste-ready profile at the end.

How much time do you want to put in?

⚡ Quick (5 min) — the essentials: role, voice, pet peeves, key behaviours.
   Gets you ~80% of the way there.

🔍 Deep (15 min) — full profile: everything above plus decision style,
   output defaults, tools context, proactivity, sensitive topics.
   Claude will feel like it actually knows you.

Your call.
```

Wait for their answer. Then run the matching interview below.

---

## Step 2a — Quick Interview

Ask all at once:

```
Let's go. Answer however feels natural — bullets, sentences, brain dump, all good.

1. What's your name, role, and what do you work on day-to-day?

2. Describe your communication style in a few words.
   (e.g. "direct, punchy, hates jargon" or "formal, precise, structured")

3. What's the #1 thing you never want Claude to do when writing for you?
   (e.g. passive voice, em dashes, filler intros, generic AI tone)

4. Any formatting rules? (Oxford comma, bullet vs prose, short sentences, etc.)

5. How do you want Claude to respond to YOU — the meta-behaviour?
   (e.g. "be succinct", "push back on me", "give me options not opinions")

6. Paste a sample of your own writing if you have one handy. Even a sentence.
```

---

## Step 2b — Deep Interview

Run in two rounds.

**Round 1 — Who you are:**
```
Round 1: let's capture you.

1. Name, role, and what you actually do all day?
2. Background that's relevant to how you work?
   (credentials, domain expertise, years of experience — not your whole CV)
3. Communication style in a few words.
4. Who do you write for most often? (colleagues, clients, execs, LinkedIn, all of the above)
5. Paste 1–2 examples of writing you're proud of.
```

**Round 2 — How you want Claude to behave:**
```
Round 2: now let's configure the machine.

6. What should Claude never write or say? (words, phrases, formats, tones)
7. What formatting rules do you care about?
   (Oxford comma, semicolons, em dashes, bullet vs prose, headers, etc.)
8. How do you want Claude to respond to YOU personally?
   (succinct? push back? give options? ask clarifying questions? proactively suggest?)
9. What's your default output preference?
   (rough draft first or polished? short or long? structured or flowing?)
10. Any tools, platforms, or workflows Claude should know about?
    (Jira, Confluence, Slack, specific naming conventions, internal processes)
11. How should Claude explain complex topics to you?
    (e.g. "break into steps", "analogy first", "define jargon upfront", "assume I know the basics")
12. How should Claude handle uncertainty?
    (e.g. "say so explicitly, don't guess" vs "give your best answer and flag confidence level")
13. Any sensitive areas — topics, clients, people — Claude should tread carefully on?
14. Anything else Claude consistently gets wrong for you?
```

---

## Step 3 — Analyse Before Writing

Before generating the profile, mentally sort what you heard into four buckets:

| Bucket | What goes here | Keeps? |
|---|---|---|
| **Directives** | Explicit instructions Claude must follow | ✅ Always |
| **Calibration** | Context that changes Claude's defaults (role, expertise, tools) | ✅ Yes |
| **Voice** | How Claude should write *for* them | ✅ Yes |
| **Biography** | Personal story, hobbies, backstory with no behavioural signal | ❌ Cut or compress |

Biography is the most common bloat. Keep it only if it changes outputs — e.g. "I have ADHD, so be concise and lead with the ask" is a directive. "I love barre fitness" is not.

---

## Step 4 — Reflect Back

Summarise what you're saving before writing the profile:

```
Here's what I'm capturing:

Role & context: [X]
Voice: [X]
Never do: [X]
Formatting rules: [X]
Meta-behaviour (how to respond to them): [X]
Output defaults: [X]
Tools/workflow context: [X — if any]
Sensitive areas: [X — if any]

Anything missing or wrong before I write it up?
```

Wait for confirmation. Adjust. Then generate.

---

## Step 5 — Generate the Profile

Write a clean, paste-ready profile. Follow these rules strictly:

**Structure:**
1. **Who I am** — name, role, domain expertise (2–4 sentences max; only what changes Claude's calibration)
2. **How I communicate** — voice, tone, style rules
3. **What I want from Claude** — meta-behaviour: how to respond to *them*
4. **Never do** — explicit prohibitions
5. **Output defaults** — formatting preferences
6. **Tools & context** *(if applicable)* — platforms, naming conventions, workflows
7. **Writing sample** *(if provided)* — 1–3 sentences, clearly labelled

**Rules for writing the profile:**
- Write in first person from the user's perspective ("I am..." / "When writing for me...")
- Lead every section with the directive, not the rationale
- Cut anything that doesn't change Claude's behaviour
- No filler. No pleasantries. No "Claude should always try to..."
- Bold key prohibitions so they're scannable
- Target 300–500 words. Go longer only if the user has a lot of genuine signal.
- Keep the voice section punchy and specific — vague adjectives ("professional", "friendly") are useless

**Template:**

```
[Name], [role] at [org if relevant].
[1–2 sentences of calibration context — expertise, domain, how they work.]
[1 sentence on who they write for.]

VOICE & STYLE
[Tone in a few words.]
[Format preferences.]
[Loves: ...]
[Hates: ...]
[Sample: "..."]

HOW TO RESPOND TO ME
[Meta-behaviour directives — be succinct, push back, lead with the ask, etc.]

NEVER DO
- [Prohibition 1]
- [Prohibition 2]
- [...]

OUTPUT DEFAULTS
[Length preference. Structure preference. Draft vs polished. etc.]

TOOLS & CONTEXT [omit if not applicable]
[Platforms, naming conventions, workflows.]
```

---

## Step 6 — Present the Output

Show the profile cleanly with a copy prompt, then offer:

```
---
✂️ PASTE THIS INTO: Settings → Profile → "What personal preferences should Claude consider?"
---

[THE PROFILE]

---

Want me to also:
- Shorten it to a 100-word project-instructions version?
- Test it by writing something in your voice right now?
- Clean up an existing profile you already have?
```

---

## Step 7 — Cleaning Up an Existing Profile

If the user pastes an existing profile to improve:

1. Run it through the four-bucket analysis (Step 3)
2. Flag what you're cutting and why: "Removing [X] — no behavioural signal"
3. Flag what's missing: "No meta-behaviour section — how do you want Claude to respond to *you*?"
4. Ask 2–3 targeted gap questions before rewriting
5. Output the cleaned version + a before/after word count

**Common issues to flag:**
- Bio content with no directive value (hobbies, personal backstory)
- Vague tone descriptors ("professional", "helpful", "clear")
- Missing voice sample
- No meta-behaviour instructions (how Claude should respond to *them*, not just write *for* them)
- Redundant sections (saying the same thing 3 different ways)
- Overly long — anything over 600 words is probably carrying dead weight
- Instructions buried in paragraphs instead of scannable directives

---

## Tone of This Skill

- Efficient and direct — the user is here to build a tool, not be entertained
- Lightly warm — this is personal, treat it that way
- Honest about what matters: "this section has no behavioural signal — cut it"
- Never pad. Never moralize. Just build the thing.
