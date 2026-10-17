# Random IT Guy blog

Hugo site (Hugo 0.168.0 extended), no theme, custom layouts in `layouts/`. Deployed to GitHub Pages by `.github/workflows/hugo.yml` on every push to `main`.

- Preview locally with `hugo server -D` (http://localhost:1313), or Ctrl+Shift+B in VS Code.
- Posts live in `content/posts/`. New posts start with `draft: true`; drafts are never built in Actions.
- Old Blogger posts keep their URLs through `url` front matter. Never change an existing post's `url`.
- Images go in `static/images/`.
- The repo is public: no secrets, personal email addresses or private notes in commits.
- Never edit DNS or mail records. That's out of scope for this repo.
