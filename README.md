# teamrat.github.io

Personal site built with [Hugo](https://gohugo.io/). Dark theme inspired by [Daring Fireball](https://daringfireball.net).

## Content Types

- **Posts** (`content/posts/`) — Linked-list style blog. Set `link:` in front matter for external links (shows ★ permalink). Leave `link` empty for regular posts.
- **Photos** (`content/photos/`) — Photo posts. Set `image:` in front matter. Drop images in `static/images/`.
- **Notes** (`content/notes/`) — Short observations, no title needed.

## Quick Start

```bash
# Install Hugo (macOS)
brew install hugo

# Create new content
hugo new content posts/my-new-post.md
hugo new content photos/sunset-december.md
hugo new content notes/quick-thought.md

# Local preview (includes drafts)
hugo server -D

# Build for production
hugo --minify
```

## Deploying

Push to `main` branch. GitHub Actions builds and deploys automatically via `.github/workflows/hugo.yml`.

### Setup (one-time)

1. Go to repo **Settings → Pages**
2. Under **Source**, select **GitHub Actions**
3. Push to `main` — the workflow handles the rest

### Custom Domain (teamrat.net)

1. Purchase `teamrat.net` from any registrar
2. Add a `CNAME` record pointing to `teamrat.github.io`
3. Add a file `static/CNAME` containing just: `teamrat.net`
4. Update `baseURL` in `hugo.toml` to `https://teamrat.net/`
5. In repo Settings → Pages, enter `teamrat.net` as custom domain

## Structure

```
.
├── hugo.toml              # Site config
├── content/
│   ├── posts/             # Blog posts & linked list
│   ├── photos/            # Photo posts
│   ├── notes/             # Short observations
│   ├── about.md           # About page
│   └── colophon.md        # Colophon page
├── layouts/               # Custom templates
│   ├── _default/          # Base templates
│   ├── partials/          # Header, footer, tags
│   ├── posts/             # Post templates
│   ├── photos/            # Photo templates
│   └── notes/             # Note templates
├── static/
│   ├── css/style.css      # All styles
│   └── images/            # Your photos
├── archetypes/            # Content templates
└── .github/workflows/     # Auto-deploy
```
