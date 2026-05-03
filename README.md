# tabtap-legal

Privacy policy and terms of service for [TabTap](https://github.com/brentlilley-lgtm/taptab) — the bill-splitting app where the receipt photo *is* the interface.

## Live site

Deployed to Vercel from this repo. Push to `main` → auto-deploy.

- Home: `/`
- Privacy policy: `/privacy`
- Terms of service: `/terms`

## What's here

```
.
├── index.html             # Landing page
├── privacy.html           # Privacy policy (rendered)
├── terms.html             # Terms of service (rendered)
├── style.css              # Shared styles (Aesop / Le Labo aesthetic)
├── vercel.json            # Clean URLs + security headers
├── privacy-policy.md      # Markdown source for privacy.html
└── terms-of-service.md    # Markdown source for terms.html
```

## Editing

For small typo fixes, edit the `.html` files directly and push.

For substantive content changes:

1. Edit the `.md` source first (so the markdown stays the source of truth)
2. Mirror the change in the corresponding `.html` file
3. Bump the `Last updated` date at the top of both
4. Note what changed in the commit message — git history is the public version log
5. Push to `main`; Vercel auto-deploys

## Stack

Pure static HTML + CSS, no build step, no JavaScript. Hosted on Vercel.

## License

Content (the policies themselves) is provided as-is for use with TabTap. Style and structure may be adapted under the MIT License.
