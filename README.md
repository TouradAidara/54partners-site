# 54 Partners

Marketing site for 54 Partners, a pan-African strategy, legal & financial advisory firm.

The site is intentionally dependency-free: one `index.html` file (markup, styles, and client-side routing/rendering logic) plus static assets in `public/`. There is no install step, build step, package manager, framework, or dev server — open `index.html` directly in a browser.

Pages (Home, Expertise, Clients, Contact) are client-rendered and addressed via hash routes (`#/expertise`, `#/clients`, `#/contact`) so navigation, direct links, and back/forward all work without a server. The contact form is front-end only — wire it up to a real backend or form/email service before relying on it to receive submissions.

## How Conductor Uses This Project

Conductor creates each workspace as its own git worktree and branch. The checked-in `.conductor/settings.toml` tells Conductor how to prepare and run this starter app:

```toml
"$schema" = "https://conductor.build/schemas/settings.repo.schema.json"

[scripts]
setup = "true"
run = "open index.html"
```

When you create a workspace, setup succeeds immediately. When you click Run on macOS, Conductor opens the HTML file in your default browser.

## Local Development

Open the app directly:

```sh
open index.html
```

Edit `index.html`, then refresh the browser.

## Project Structure

- `index.html` contains the UI, styling, and interaction logic.
- `public/` contains static assets used by the page.
- `.conductor/settings.toml` contains the shared Conductor workspace scripts.
- `.context/` is available in Conductor workspaces for gitignored notes and handoff files between agents.

## Learn More

- [Conductor docs](https://conductor.build/docs)
