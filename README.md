# Client Close Kit

Landing page for **Client Close Kit** by Leo Ching — a practical client workflow for freelancers.

**Buy on Gumroad:** https://chingleo.gumroad.com/l/client-close-kit

**Intended live site:** https://ching1010.github.io/client-close-kit/

## Enable GitHub Pages (one-time)

Site files are already on the `gh-pages` branch. Until Pages is turned on, that URL returns 404.

1. Open https://github.com/ching1010/client-close-kit/settings/pages
2. Under **Build and deployment** → **Source**, choose **Deploy from a branch**
3. Branch: **gh-pages** / **/** (root) → Save

Or with a `repo`-scoped token:

```bash
gh api -X POST repos/ching1010/client-close-kit/pages \
  -f build_type=legacy \
  -f source[branch]=gh-pages \
  -f source[path]=/
```

After that, pushes to `main` redeploy via `.github/workflows/static.yml` (peaceiris → `gh-pages`).
