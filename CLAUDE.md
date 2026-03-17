# CLAUDE.md

This repo hosts redirect pages on GitHub Pages at `octionary.github.io/redirect/`.

## Structure

```
redirect/
├── index.html                        # Root redirect
├── netcast-poster-2026/
│   └── index.html                    # Poster redirect
└── <new-path>/
    └── index.html                    # Add more like this
```

## Changing a redirect target

Edit the `index.html` in the relevant directory. Update the URL in **both** places:

```html
<meta http-equiv="refresh" content="0; url=NEW_URL">
<script>window.location.href = "NEW_URL";</script>
```

## Adding a new redirect

1. Create a new directory with an `index.html`:

```html
<!DOCTYPE html>
<html>
<head>
  <meta http-equiv="refresh" content="0; url=TARGET_URL">
  <script>window.location.href = "TARGET_URL";</script>
</head>
<body>
  <p>Redirecting...</p>
</body>
</html>
```

2. Update the "Active redirects" table in `README.md`
3. Commit and push to `main` — GitHub Pages deploys automatically
