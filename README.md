# Gutsu's Time

A professional, public time-tracking dashboard and blog powered by [Timewarrior](https://timewarrior.net/) and GitHub Pages.

## Live Site

Visit: `https://<user>.github.io/Timew/`

## Structure

```
├── index.html          # Dashboard (Stats, Blog, Videos)
├── all-time.json       # Timewarrior export data
├── posts/
│   ├── index.json      # Blog post manifest
│   └── *.md            # Markdown blog posts
├── videos/
│   ├── index.json      # Video manifest
│   └── *.mp4           # Video files
└── README.md
```

## How It Works

1. The dashboard auto-fetches `all-time.json` on every page load — no manual upload needed
2. Blog posts are Markdown files listed in `posts/index.json`
3. Videos are MP4 files listed in `videos/index.json`

## Publishing Content

### Time Stats
```bash
timew export > all-time.json
git add all-time.json && git commit -m "update stats" && git push
```

### Blog Posts
1. Write a `.md` file in `posts/`
2. Add an entry to `posts/index.json`:
```json
{ "file": "my-post.md", "title": "Post Title", "date": "2026-08-31", "summary": "Brief description." }
```
3. Push to GitHub

### Videos
1. Place `.mp4` files in `videos/`
2. Add an entry to `videos/index.json`:
```json
{ "file": "demo.mp4", "title": "Demo Video" }
```
3. Push to GitHub
