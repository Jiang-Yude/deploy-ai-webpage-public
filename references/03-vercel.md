# Vercel Workflow

Vercel is useful for fast sharing, previews, front-end frameworks, and projects that may later need serverless functions.

## Beginner Flow

1. Create or log in to a Vercel account.
2. Import a Git repository, or use Vercel CLI.
3. Confirm the project root.
4. Deploy.
5. Open the production URL.

The generated URL usually looks like:

```text
https://project-name.vercel.app
```

## CLI Flow

Use this when Vercel CLI is installed and authenticated.

```bash
vercel
```

For production:

```bash
vercel --prod
```

After deployment, verify the URL:

```bash
curl -I "https://YOUR-PROJECT.vercel.app"
```

## Static HTML Notes

For a simple static page, the folder should include:

```text
index.html
style.css
script.js
assets/
```

Vercel can serve static files directly. Framework projects may require build settings. If the user is using Next.js, Vite, Astro, SvelteKit, or another framework, inspect `package.json` before deploying.

## Common Problems

### Wrong Folder Deployed

Symptoms:

- The deployed page is blank.
- The deployed page is an old version.
- The page shows a directory or framework default.

Fix:

- Confirm the actual project root.
- Deploy from the folder that contains the current `index.html` or framework config.
- For versioned folders, deploy from the current version folder, not the parent folder.

### Images Missing

Check:

- Assets are inside the deployed folder.
- HTML paths are relative.
- File names match exactly.

### Private Content Concern

Treat beginner Vercel deployments as public unless protection is intentionally configured. If the page contains sensitive information, pause and choose an appropriate protected workflow.

## Save To Personal Notes

After deployment, save:

- project name
- production URL
- whether CLI or Git import was used
- build settings
- any fix needed
