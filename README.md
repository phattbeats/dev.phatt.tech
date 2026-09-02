# dev.phatt.tech

Source for [https://dev.phatt.tech](https://dev.phatt.tech), the public developer/vendor page for PHATT Tech LLC.

A flat static site. Plain HTML and CSS, no build step, no JavaScript runtime, no analytics.

## Structure

```
.
├── index.html          # Home / Work
├── projects/index.html # Projects (proof of work)
├── docs/index.html     # Docs (placeholder, real entries come later)
├── contact/index.html  # Contact
├── 404.html
├── styles/main.css
├── CNAME               # dev.phatt.tech
└── LICENSE             # MIT
```

## Editing

Edit the HTML and CSS directly. No bundler, no framework. Preview by serving the directory locally:

```sh
python3 -m http.server 8000
```

Then open `http://localhost:8000/`.

## Deploy

Pushed to the `main` branch of `phattbeats/dev.phatt.tech`. GitHub Pages serves it. The `CNAME` file binds the custom domain `dev.phatt.tech`; the DNS record (a CNAME pointing to `phattbeats.github.io`) is a separate, operator-owned action.

## Content rules

The page is on the `.tech` domain and speaks only about the business and its public work.

- No employer, client, subsidiary, or proprietary system names.
- No internal hostnames, IPs, container names, or infrastructure details.
- Link only to repos verified public by unauthenticated fetch.
- Contact is `brandon@phatt.tech` only.
- No credentials, keys, or webhook URLs anywhere.

A pre-deploy grep enforces these rules. The constraint-word regex is documented in the issue tracker under the project for this site.
