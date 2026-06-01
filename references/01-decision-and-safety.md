# Decision And Safety Guide

## Start Here

Ask three questions:

1. Can this page be public?
2. Does it need only static hosting?
3. Does the user care more about long-term public publishing or fast sharing?

## Platform Choice

### Use GitHub Pages When

- The page is a public work, portfolio, teaching demo, article companion, event page, or documentation page.
- The user is comfortable creating a GitHub repository.
- The project is static: `index.html`, CSS, JavaScript, images.
- A stable URL like `https://username.github.io/repo-name/` is acceptable.

### Use Vercel When

- The user wants a quick shareable prototype URL.
- The project uses a front-end framework or may later need serverless functions.
- The user wants easy preview deployments.
- The user is already logged in to Vercel CLI or connected to Vercel through Git.

### Pause Before Deploying When

- The page contains private, client, or internal content.
- The user asks for password protection, access control, or private sharing.
- The project contains secrets such as API keys or tokens.
- The user is unsure whether the content is safe to publish.

## Beginner Privacy Explanation

Free deployment is useful, but beginners should treat it as public unless they intentionally configure protection.

Simple rule:

- Public teaching example: okay.
- Portfolio or activity page: okay.
- Client report, meeting notes, private proposal: pause.
- Anything with secrets: remove before deployment.

## Preflight Checklist

Before deploying, confirm:

- `index.html` exists at the folder root.
- Images and CSS files are included.
- Links are relative or point to public URLs.
- No `.env`, token file, database, or private export is included.
- The page title is appropriate.
- The page works locally.

## Post-Deploy Checklist

After deploying, confirm:

- The final URL opens.
- Images load.
- CSS loads.
- Links work.
- The page looks acceptable on mobile.
- The user has saved the URL.
- Any lesson learned is added to personal notes.
