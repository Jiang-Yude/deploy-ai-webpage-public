# GitHub Pages Workflow

GitHub Pages is a good default for public static webpages.

## Beginner Flow

1. Create or choose a GitHub repository.
2. Put `index.html` and all assets in the repository.
3. Push to the main branch.
4. In GitHub repository settings, open Pages.
5. Choose source: deploy from branch.
6. Select `main` and `/root`.
7. Wait for GitHub to publish.
8. Open the final URL.

The final URL usually looks like:

```text
https://USERNAME.github.io/REPOSITORY/
```

## Agent-Assisted CLI Flow

Use this only when the user has GitHub CLI installed and authenticated.

```bash
git init -b main
printf ".DS_Store\nnode_modules/\n.env\n.vercel/\n" > .gitignore
git add .
git commit -m "init: deploy static webpage"
gh repo create REPOSITORY --public --source=. --push
gh api -X POST "repos/USERNAME/REPOSITORY/pages" \
  -f "source[branch]=main" \
  -f "source[path]=/"
```

Then verify:

```bash
curl -I "https://USERNAME.github.io/REPOSITORY/"
```

## Common Problems

### Page Shows 404

Check:

- Pages is enabled.
- The branch is correct.
- `index.html` is at the publishing root.
- The repository name in the URL is correct.
- The first build may still be running.

### CSS Or Images Missing

Check:

- File names match exactly, including case.
- Paths are relative.
- Assets were committed and pushed.
- The HTML does not point to a local `file://` path.

### User Accidentally Published Private Content

Immediately remove the content, commit, and push. If sensitive data was exposed, rotate affected secrets. For truly private content, use a protected hosting setup instead of public GitHub Pages.

## Save To Personal Notes

After every successful or failed deployment, save:

- repository name
- final URL
- what went wrong
- exact fix
- commands that worked
