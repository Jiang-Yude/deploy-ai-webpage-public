---
name: deploy-ai-webpage-public
description: Public beginner skill for helping users publish an AI-made static webpage to a shareable URL with GitHub Pages or Vercel. Use when the user wants to deploy an HTML/CSS/JS webpage, choose between GitHub Pages and Vercel, set up a public sharing workflow, troubleshoot common deployment issues, or maintain their own personal deployment notes.
---

# Deploy AI Webpage Public

This is a public, beginner-friendly skill for turning an AI-made webpage into a shareable URL.

It is designed for static webpages: HTML, CSS, JavaScript, images, and other front-end files. It does not assume any private knowledge base, internal folder structure, or personal account details.

## Core Rule

Before deployment, always ask or check:

1. Is this page safe to be public?
2. Is there an `index.html` at the deploy root?
3. Does the page need GitHub Pages or Vercel?
4. After deployment, does the final URL open successfully?
5. What did we learn that should be saved into personal notes?

## Choose A Path

Use this quick selection:

| Situation | Use |
|---|---|
| Public portfolio, teaching material, public demo, simple static page | GitHub Pages |
| Fast prototype sharing, no need to manage GitHub Pages settings manually | Vercel |
| Dynamic API, serverless functions, framework app, preview deployments | Vercel |
| Sensitive or private content | Stop and discuss privacy protection before deploying |

For the full decision guide, read `references/01-decision-and-safety.md`.

## Workflow

1. Inspect the folder.
   - Confirm the deploy root.
   - Confirm `index.html` exists.
   - Confirm assets use relative paths when possible.
   - Confirm no obvious private data is included.

2. Pick the platform.
   - GitHub Pages: read `references/02-github-pages.md`.
   - Vercel: read `references/03-vercel.md`.

3. Deploy.
   - Run the smallest reliable workflow for the chosen platform.
   - Do not expose tokens, team IDs, private paths, or secrets.
   - Prefer public-safe defaults for beginner use.

4. Verify.
   - Open the final URL.
   - Check the page, images, links, and mobile layout.
   - If it fails, use the troubleshooting section in the relevant reference.

5. Update personal notes.
   - Read `references/04-personal-notes-template.md`.
   - Add project-specific preferences, account setup notes, common fixes, and favorite commands.
   - Keep secrets out of notes.

## Public Safety Checklist

Before publishing, scan for:

- real customer names
- private meeting notes
- private prices or proposals
- phone numbers, email addresses, home addresses
- API keys, tokens, `.env` files
- unpublished strategy or confidential plans

If any appear, pause and ask whether to remove, anonymize, or use a protected deployment option.

## Useful User Prompts

```text
Help me deploy this AI-made webpage. First check whether the folder has an index.html and whether the content is safe to publish. Then recommend GitHub Pages or Vercel.
```

```text
Deploy this folder to GitHub Pages and give me the final shareable URL. If anything fails, explain the exact fix.
```

```text
Deploy this folder to Vercel and give me the production URL. After deployment, verify the page opens correctly.
```

```text
I ran into a deployment problem. Please diagnose it, fix the smallest thing needed, and save the lesson into my deployment notes.
```
