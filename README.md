# randomitguy.com

The Random IT Guy blog, converted from the Blogger export on 2026-10-17. It builds with plain Hugo and needs no theme.

- Posts are in `content/posts/`. Each keeps its old Blogger address through the `url` front matter, so old links still work.
- Images are in `static/images/`, copied from the Blogger albums export.
- Drafts (`draft: true`) are left out of the production build. New posts start as drafts.

## Preview locally

    hugo server -D        # -D includes drafts

In VS Code, Ctrl+Shift+B runs the same thing (see `.vscode/tasks.json`).

## Publish (GitHub Pages)

1. The repo is public on GitHub (free Pages needs a public repo). Pushing to `main` deploys.
2. `.github/workflows/hugo.yml` builds and deploys on every push. In the repo, Settings > Pages > Source is set to "GitHub Actions".
3. In Settings > Pages, set the custom domain to `www.randomitguy.com` and tick "Enforce HTTPS" once the certificate is ready.
4. DNS for randomitguy.com: a `www` CNAME pointing to `<your-github-username>.github.io`, and four A records on `@` for 185.199.108.153, 185.199.109.153, 185.199.110.153 and 185.199.111.153. GitHub then sends the bare domain to www.
5. Verify the domain under your GitHub profile > Settings > Pages, so no one else can claim it.

## Visitor stats

Set `goatcounter` under `[params]` in `hugo.toml` to your GoatCounter code. It's cookieless, free for personal sites, and only loads on the production build.
