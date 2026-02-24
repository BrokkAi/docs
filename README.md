# Brokkumentation

Documentation source files for [Brokk](https://brokk.ai).

## Structure

```
├── *.md           # Documentation pages (markdown)
└── images/        # Screenshots and diagrams
```

## How It Works

The Brokk webapp backend fetches these markdown files from GitHub, converts them to HTML, and serves them via API. Content is cached for 1 hour.

## Adding/Editing Documentation

1. Edit markdown files directly in this repo
2. Place images in `images/` and reference as `![](images/filename.png)`
3. Changes go live within 1 hour (cache TTL)
