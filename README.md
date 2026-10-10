# Homepage

Static website deployed to the Cloudflare Worker `homepage`.

`wrangler.jsonc` manages the custom domains `hetzmannseder.dev` and
`www.hetzmannseder.dev`. The `homepage.hetzmannseder.workers.dev` address
remains enabled. Domain bindings belong to this repository; the homelab's
OpenTofu configuration does not manage them.

The apex address currently redirects to `www.hetzmannseder.dev`; both
hostnames are bound to the Worker. The page redirects visitors to LinkedIn.

Deploy from this directory:

```bash
npx wrangler login
npx wrangler deploy --dry-run
npx wrangler deploy
```

`.assetsignore` limits public uploads to `index.html`, `style.css`, and
`robots.txt`. Add new public assets there when extending the site.
