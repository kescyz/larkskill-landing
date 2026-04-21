# larkskill-landing

Temporary "Coming Soon" page served at <https://larkskill.app> while the real
marketing landing is designed.

## Deploy

Single static `index.html`. Deploy via Cloudflare Pages Direct Upload:

```bash
npx wrangler pages project create larkskill-landing --production-branch main
npx wrangler pages deploy . --project-name larkskill-landing
```

Then in the Cloudflare dashboard, bind the custom domain `larkskill.app` to the
`larkskill-landing` Pages project (remove the binding from the old
`larkskill.pages.dev` project if it still holds it).

## Replace later

When the real landing page is ready, either:
- Push a new build into this repo and let Pages auto-deploy, or
- Create a new CF Pages project and rebind `larkskill.app`.

## What was here before

`larkskill.app` was previously bound to the `larkskill.pages.dev` CF Pages
project, sourced from `kescyz/kesflow-user-token-management`'s `portal/`
subdir (v1 portal). That deploy is superseded by `portal.larkskill.app`
(v2 portal, sourced from `kescyz/larkskill-v2`).
