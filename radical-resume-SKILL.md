---
name: radical-resume
description: >
  Generate a "Radical Resume" — a personality-forward, brutally honest
  version of a professional resume, in the style of Vanessa Devine's viral
  LinkedIn post ("Radical Resume™"). ALWAYS trigger when Keddy says "radical
  resume," "make my resume radical," or references the Vanessa Devine /
  spicy resume format. Loosely inspired by a normal resume's building
  blocks (Summary, Skills, Experience, Keywords, Education) but rewritten
  in the user's own brand of "radical" — voice, visual style, AND structure
  are all elicited first, never assumed or copied from Vanessa's original.
  This is a cathartic/for-fun artifact, NOT an ATS submission doc — always
  confirm that with the user before treating it as a real application doc.
---

# Radical Resume Skill

## What this is

Inspired by Vanessa Devine's viral "Radical Resume™": same bones as a real
resume (Summary → Skills → Experience → ATS Keywords → Education) but every
line is rewritten in a specific, deliberate flavor of "too honest for
LinkedIn." Vanessa's flavor was profanity. That's ONE flavor, not THE
format — the skill's whole job is finding the user's flavor before writing
a word.

**Never default to profanity/swearing as the style.** That's copying
Vanessa's résumé, not making the user's own. Always ask first.

---

## Step 1 — Get the source content

Check if a resume already exists in this conversation, Project Knowledge,
or Google Drive. If not, ask the user to paste their current resume or
bullet points. Don't write filler experience — real accomplishments only,
never invented ones.

---

## Step 2 — Elicit their "brand of radical"

Use `ask_user_input_v0`. Never assume — offer options, since Keddy always
wants multiple choice. Suggested flavors (pick ~4 to show, rotate/mix as
relevant, always include "combo" and "something else"):

- **Profanity / brutal honesty** — Vanessa's original. Swearing, zero corporate filter.
- **Unhinged pop culture** — every line is a movie quote, meme reference, or "main character energy."
- **CAPS LOCK & !!! chaos** — excessive punctuation, all-caps for emphasis, exclamation-point overload.
- **Skills as mini-stories** — instead of bullet fragments, each skill is a 1-2 sentence anecdote/mini-scene.
- **Self-deprecating comedy** — undercut every achievement with a joke at your own expense, Michael Scott energy.
- **Corporate jargon roast** — use the buzzwords ("synergy," "circle back") ironically while mocking them in the same breath.
- **Deadpan/dry** — flat, matter-of-fact delivery of absurd truths, no exclamation points at all.
- **Emoji chaos** — visual noise, emoji punctuation on every line.
- **Combo** — mix two of the above.
- **Something else** — let them describe it.

Ask this as ONE question, single-select, options capped at 4 per the tool —
if showing more flavors, split into a couple of quick single-select
questions rather than overloading one.

Also confirm real quick: is this for actual job applications, or purely a
just-for-fun/catharsis piece? (Changes the disclaimer at the end, and
whether "Keywords for ATS" section should be real keywords or a joke.)

---

## Step 3 — Elicit the visual theme

Don't default to Vanessa's purple-serif-minimalist look. That's her
radical, not the user's. Ask (multiple choice, one question, cap 4
options + let them pick more than one round if needed):

**Overall look:**
- **Minimalist/editorial** — Vanessa's original: serif, thin rules, lots of white space
- **Bold maximalist** — big color blocks, oversized type, zero white space
- **Dark mode** — dark background, high-contrast neon or pastel text
- **Zine/scrapbook** — collage-y, hand-drawn dividers, sticker-tag vibes (use sparingly — check in after showing a draft, this one runs "gimmicky" fast; see note below)
- **Retro/vintage** — typewriter fonts, cream paper texture, stamp/postcard motifs
- **Painterly/art-inspired** — pull palette and motifs from a real reference (their own moodboard, a Pinterest board, art they like) rather than a generic "theme name"
- **Their own established brand** — if they have a personal design system already (colors/fonts they use elsewhere), offer to apply that instead
- **Surprise me** — pick something that fits their voice flavor from Step 2

**Ask if they have visual references.** Before picking a theme name off a
list, ask if they have images to pull from — a moodboard, a Pinterest
board screenshot, art they love, an existing brand. A real reference beats
a theme label every time: it gives actual colors, motifs, and a feel to
extract rather than a generic interpretation of "zine" or "maximalist."
If they share images, name the specific colors and motifs you're pulling
(e.g. "sunset coral/gold/teal, gestural florals, wave line-art") back to
them before building, so the direction is confirmed, not assumed.

**Color + font, once look is picked:** if there's no reference image,
offer 3-4 concrete combos rather than asking open-ended ("pick a color")
— e.g. for bold maximalist: "hot pink + black," "electric blue + orange."
Concrete choices beat open questions for a fast yes/no decision.

If the person has a personal design system already established (check
memory/Project Knowledge for one), surface it as an explicit option but
never auto-apply it — Radical Resume is allowed to be a totally different
animal from their day-to-day brand. If they want their own brand "but
bigger" (extra accent colors added on top), that's a legitimate answer —
build the extension, don't just replay their existing palette unchanged.

**Note on "gimmick" themes:** literal theme executions (actual washi tape,
actual torn paper, actual confetti dots) can read as try-hard rather than
stylish once built, even when the theme name sounded fun in the abstract.
If a themed build doesn't land, don't just re-skin the same layout with
different stickers — go back to a reference image or a cleaner design
language (gradients, line art, soft shadows) instead of doubling down on
the literal craft-object metaphor.

---

## Step 4 — Rewrite content in that voice AND structure

The Summary → Skills → Experience → Keywords → Education shape is a
starting suggestion, not a rule. Once voice and visual theme are locked,
ask if they want the standard shape or something weirder — e.g.:

- Reordered sections (skills-first, experience-as-a-timeline, etc.)
- Renamed sections that match the voice (not just "Skills" → also consider things like "A Brief Timeline of Chaos," "Things I Will Not Apologize For," "Receipts")
- Non-linear layout — a "choose your own adventure" career path, a highlight reel instead of chronological jobs
- **Experience as short stories** — instead of Title | Dates | bullets per role, 3-5 short narrative vignettes (2-4 sentences each), one per notable arc rather than one per employer. Real facts, story delivery. This reads much less "resume-like" than a bulleted block per job — reach for it whenever the person wants this to feel more like a fun read than a document.
- Extra invented sections that don't exist on normal resumes (a "warning labels" section, a "known bugs" section, whatever fits their voice)
- Dropped sections that don't serve the joke (e.g. skip Keywords for ATS and a formal Education block entirely if this is pure catharsis — they're the most "actual resume"-coded sections and cutting them does more to sell the bit than any joke can)

**Ask upfront whether this should read like an actual resume at all**, or
be something shorter and more narrative that just borrows a resume's
shape. Don't assume the full Summary/Skills/Experience/Keywords/Education
shape is wanted — a lot of the fun is in how far it departs from that.

Whatever shape is chosen:
- Rewrite EVERY line in the chosen voice — don't just reskin headers and leave bullets corporate.
- Keep real accomplishments; change the delivery, not the facts.
- **Watch for accidental repetition** — recurring bits/callbacks (a catchphrase, a named reference) are fine used deliberately once or twice across the whole piece, but re-check the full draft for the same joke or phrase landing twice by accident, especially in Summary vs. Experience sections written in separate passes.
- Show a draft of 2-3 sections first if the resume is long, so voice AND structure get approved before the full build — cheaper to fix 3 bullets than rewrite 20.
- Default to shorter over longer. A radical resume that's exactly as long as the real one just feels like a corporate document with jokes in it — trimming hard is part of what makes it feel fun rather than exhausting to read.

**Audience awareness:** ask (or check memory) whether this might be seen
by clients, colleagues, or anyone professional — e.g. posted on LinkedIn,
sent around at work. If so, keep the voice itself client-safe (the
established flavor from Step 2 doesn't need to change, just don't let
content drift into anything that reads badly to a professional audience)
and drop personal contact info (phone, email, address) unless there's a
real reason to keep it — this is a personality piece, not a place to
broadcast contact details.

---

## Step 5 — Ask output format

Ask (multiple choice, per Keddy's preference):
- **Word doc (.docx)** — editable, most portable
- **Just show it here in chat** — markdown, quick and cathartic, no file
- **HTML artifact** — best fit if the visual theme is bold/maximalist/zine and needs layout docx can't easily do (color blocks, custom layout, dark mode)
- **Google Doc** — if they want it in Drive/shareable via Google. Upload with `Google Drive:create_file`, `contentMimeType: "text/html"`, the built HTML as `textContent` (or base64 `content` for special characters/emoji), and leave conversion to Google Docs on default (don't set `disableConversionToGoogleType`). Heads up when offering this: Google's HTML import keeps text, structure, bold/italic/color reasonably well but will NOT preserve custom fonts, gradients, box-shadows, or precise layout (waves/blobs/rotation) — it's a fair option for a themed-but-simple build (editorial/retro), a poor fit for a maximalist HTML build with heavy CSS. Say that trade-off up front rather than let them be surprised by a flattened doc.

Let the chosen visual theme drive this: docx and Google Doc are fine for editorial/retro/minimalist looks; a genuinely maximalist or zine/painterly HTML build won't survive conversion to either and should just stay an HTML artifact (or get offered as a "flattened" secondary export, clearly labeled as simpler than the original). Ask, don't assume.

---

## Step 6 — Build

If docx: follow `/mnt/skills/public/docx/SKILL.md` conventions (paragraph
borders for horizontal rules, not tables; numbering config for bullets;
verify render with soffice + pdftoppm before presenting). Save to
`/mnt/user-data/outputs/` and call `present_files`.

If HTML artifact: build to match the chosen theme's colors/fonts/layout —
this is the right call when the theme is more visually ambitious than a
standard document layout supports.

If chat-only: just render in the response, no file needed.

---

## Step 7 — Disclaimer (only if this might go anywhere real)

If Step 2 confirmed this is for actual applications, close with a quick,
non-nagging one-liner: something like "Just flagging — this version's for
you, not ATS. Want a toned-down cover-letter version too?" Skip entirely
if it's confirmed just-for-fun.

---

## Step 8 — Iterating after the first build

This is a living document, not a one-shot generation — expect several
rounds of "change the font," "I don't like this theme, try again," "here's
my own rewrite of the content, apply it." Treat the working file as
persistent and edit it in place rather than regenerating from scratch each
time:

- **Style-only requests (font, color, spacing) → touch only CSS/style, never regenerate content.** If the person asks for a font swap or color change, use `str_replace` on the relevant style block(s) and leave every line of copy untouched. After any style-only edit, it's worth a quick grep/search for a couple of distinctive phrases from their content to confirm nothing was dropped — style edits are exactly the moment content regressions sneak in unnoticed, and the person may not immediately spot a missing line in a long resume.
- **When the person hands back their own rewritten content** (pasted text, tracked-style edits, a full rewrite), apply it close to verbatim — fix only obvious typos, don't paraphrase or "improve" their wording. It's their voice, not a draft for Claude to polish. Preserve any real quotes they include (properly short, properly attributed) and any emoji they describe by name (e.g. "muscle emoji," "proud emoji") — pick the closest real emoji and use it, don't leave a placeholder.
- **When a theme/font swap is rejected, don't argue for it** — revert cleanly and try the next direction. Multiple rounds of "no, try again" on visual style is normal for this format; the person's taste is the only spec that matters.
- **Two kinds of visual reference are useful and often given separately:** a moodboard/art board (for palette + motifs, e.g. "sunset coral/gold, wave line-art") and actual example resumes/documents (for layout, font pairing, and formatting ideas — two-column sidebars, pill tags, icon bullets, chunky display fonts). If given real resume examples, name the specific formatting moves being borrowed (e.g. "chunky rounded display font for the name, icon-badge skill list, colored accent bar per section") back to the person before rebuilding.
- **Give meta/aside content its own visual treatment by default** — an "also, some non-resume facts about me" aside, a footer sign-off line, or any other content that isn't core resume material reads as more fun and stands out more when it gets its own callout card, colored banner, or badge treatment rather than blending into body text as small italic type. This is worth doing proactively, not just when asked.
- **If asked for "the raw content"** (so they can edit it themselves), give clean plain text/markdown with clear section labels, no HTML/CSS — this is for them to mark up and hand back, not a deliverable to present as a file.

---

## Notes

- The whole value of this format is specificity and honesty, not just
  swearing. A "radical resume" that just adds curse words to bland bullets
  misses the point — the bullets themselves need real personality.
- Keep it to the user's real accomplishments. Radical ≠ fabricated.
- If Keddy invokes this for someone else (a friend, gift), still run Step 2
  for THAT person's flavor — ask Keddy to relay it if the friend isn't in
  the chat.
