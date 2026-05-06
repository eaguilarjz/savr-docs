# Deploying savr Docs to GitHub Pages

The docs site lives at the root of the repository and is served via GitHub Pages at the custom domain `docs.savr.pro`. Language detection is handled client-side with a small JavaScript redirect in `index.html`.

---

## One-time setup

1. Push your changes to the `main` branch on GitHub.
2. Open the repository on GitHub and go to **Settings → Pages**.
3. Under **Build and deployment**, set:
   - **Source**: `Deploy from a branch`
   - **Branch**: `main`
   - **Folder**: `/ (root)`
4. Click **Save**.
5. Under **Custom domain**, enter `docs.savr.pro` and save. The repo's `CNAME` file at the root must contain the same value.

GitHub will build and publish the site. After a minute or two it will be available at:

```
https://docs.savr.pro/
```

The default Pages URL `https://eaguilarjz.github.io/savr-docs/` will 301-redirect to the custom domain.

---

## How i18n works (the workaround)

GitHub Pages serves static files only — there is no server-side logic. True i18n (e.g. reading the `Accept-Language` HTTP header) is not available.

The workaround uses a JavaScript redirect in `index.html`:

```js
var lang = (navigator.language || navigator.userLanguage || 'en').toLowerCase();
var dest = lang.startsWith('es') ? './es/' : './en/';
window.location.replace(dest);
```

### What happens step by step

| Step | What occurs |
|---|---|
| User visits `/` | GitHub Pages serves `index.html` |
| JS runs | `navigator.language` is read (e.g. `"es-MX"`, `"en-US"`) |
| Redirect | User is sent to `/es/` or `/en/` immediately |
| Fallback | If JS is disabled, two manual links are shown (`English` / `Español`) |

### Language coverage

| Browser language | Redirects to |
|---|---|
| `es`, `es-MX`, `es-AR`, `es-*` | `/es/` |
| Everything else | `/en/` |

To add more languages in the future, add a new folder (e.g. `fr/`) and extend the redirect logic in `index.html`.

### Cross-page language links

Every page in `en/` has a link at the top pointing to the equivalent page in `es/`, and vice versa. These are relative Markdown links that work both on GitHub (rendered Markdown) and on the Pages site (Jekyll).

---

## Updating the docs

1. Edit any `.md` file under `en/` or `es/`.
2. Commit and push to `main`.
3. GitHub Actions rebuilds and deploys automatically — no manual step needed.

---

## Local preview

To preview the docs locally with Jekyll:

```bash
gem install bundler jekyll
jekyll serve
# Open http://localhost:4000
```

Or, since the files are plain Markdown, any Markdown preview tool works — including the GitHub web UI and VS Code's built-in preview.

---

## Limitations of the client-side approach

- **No SEO language tagging** — search engines may not associate `/es/` pages with Spanish-speaking users automatically. Mitigate by adding `<html lang="es">` to each page (requires Jekyll front matter or a custom layout).
- **Redirect flicker** — the user briefly sees the landing page before being redirected. The redirect is instant in practice but not invisible.
- **No cookie memory** — each visit re-reads `navigator.language`. If a Spanish speaker's browser is set to English they always land on `/en/`. There is no language toggle that persists a preference.
