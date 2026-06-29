# Blog Writing Guide — Configr Stdio

This guide covers everything you need to write and publish a blog post on the Configr Stdio site. No coding knowledge required.

---

## How it works

1. Write the post (Google Docs, Notion, wherever you prefer)
2. Create a new `.md` file in `src/content/blog/` — filename becomes the URL slug
3. Paste in the frontmatter block at the top (see below)
4. Paste your content below it using Markdown formatting
5. Set `draft: false` when ready to publish
6. Commit and push — Vercel auto-deploys in ~30 seconds

---

## File naming

The filename = the URL. Keep it lowercase, words separated by hyphens, no spaces.

```
src/content/blog/5-salesforce-mistakes-smbs-make.md
→ configrstdio.com/blog/5-salesforce-mistakes-smbs-make
```

---

## Frontmatter block

Every post must start with this block at the very top:

```markdown
---
title: "Your Post Title Here"
description: "One sentence summary shown on the blog listing page and in Google search results."
publishDate: 2026-08-01
author: "John Michael Mahaguay"
tags: ["Salesforce", "Tips"]
draft: false
---
```

| Field | Notes |
|---|---|
| `title` | Full post title. Keep under 60 characters for SEO. |
| `description` | One sentence. Shown on listing page and Google. Make it compelling. |
| `publishDate` | Format: `YYYY-MM-DD`. Can be a future date. |
| `author` | Leave as-is unless posting changes. |
| `tags` | 2–4 short tags. Shown as pills on the post. |
| `draft` | Set `true` while writing. Flip to `false` to publish. |

---

## Markdown formatting

### Headings

```markdown
# Heading 1 — page title (don't use — the post title handles this)
## Heading 2 — main sections
### Heading 3 — subsections
```

### Paragraphs

Just write. Leave a blank line between paragraphs.

### Bold & Italic

```markdown
**bold text**
*italic text*
***bold and italic***
```

### Lists

```markdown
- Bullet point
- Another point
  - Indented sub-point

1. Numbered list
2. Second item
3. Third item
```

### Links

```markdown
[link text](https://example.com)

# Link to the contact section on the site:
[get in touch](/#contact)
```

### Horizontal divider

```markdown
---
```

### Blockquote (for callouts or quotes)

```markdown
> This is a blockquote. Good for highlighting a key insight.
```

---

## Content structure that works well

```
Intro — hook the reader, state the problem
---
## Section 1
## Section 2
## Section 3
---
## Closing thought / common thread
CTA line linking to /#contact
```

See `src/content/blog/5-salesforce-mistakes-smbs-make.md` as a reference example.

---

## SEO guide

Unlike LinkedIn posts that die in 48 hours, blog posts get found on Google for years. These habits compound over time — the more consistently you apply them, the more traffic builds.

### One post = one keyword

Before writing, ask: *what would someone type into Google to find this?* That phrase is your keyword. Work it naturally into:
- The title
- The first paragraph
- One or two section headings

**Good target keywords:**
- "salesforce implementation for small business"
- "salesforce admin vs consultant"
- "how long does salesforce implementation take"
- "salesforce crm setup guide"

Don't try to target multiple keywords in one post — one post, one topic, done well.

### Title craft

The title is the single most important SEO element. Format that works:

```
[Specific Problem] — [Who It's For]
```

Examples:
- ✅ "5 Salesforce Mistakes SMBs Make (And How to Fix Them)"
- ✅ "What to Expect From a Salesforce Implementation: A Business Owner's Guide"
- ❌ "Our Thoughts on Salesforce"

Rules:
- Always include the word "Salesforce" — that's the keyword you're building authority around
- Lead with the problem, not the solution
- Keep it under 60 characters or Google cuts it off

### Description as a click-ad

The description doesn't affect ranking directly — but it affects whether someone clicks your result, which does. Write it like you're selling the click in one sentence:

- ❌ "This article discusses common Salesforce implementation issues."
- ✅ "Most Salesforce projects fail in the first 30 days. Here's what goes wrong — and how to avoid it."

Under 155 characters. Compelling over clever.

### The first 100 words matter most

Google weights the intro heavily. State the topic and the reader's problem in the very first paragraph — don't warm up slowly. Get to the point immediately.

### Links work both ways

- **Link in** — include at least one link to `[get in touch](/#contact)` or `[our services](/#services)` per post. This passes authority to the pages that generate leads.
- **Link out** — when referencing a Salesforce feature or edition, link to the official Salesforce documentation. It signals credibility to Google.

### Content length

600–1200 words is the sweet spot. Longer is fine if every paragraph earns its place. Short is fine if the topic is narrow. Never pad for length.

### Images (when we add them)

Every image needs an `alt` attribute describing what it shows — Google reads alt text. When adding images to a post, the format is:

```markdown
![A screenshot showing the Salesforce opportunity pipeline view](./pipeline-screenshot.png)
```

The text inside `[...]` is the alt text. Be descriptive, not generic ("screenshot" alone is useless).

---

## Posting cadence

One post per month. That's 12 posts in year one — enough to build domain authority without burning out.

**Repurposing loop:**
Blog post → LinkedIn summary → link back to site → visitor sees services → inquiry

---

## Questions?

Ping John to review for technical accuracy before flipping `draft: false`.
