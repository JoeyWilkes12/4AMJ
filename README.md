# 4AMJ

Tiny GitHub Pages redirect site.

## Current redirect

This repository redirects visitors to:

https://history.churchofjesuschrist.org/chd/individual/william-henry-adams-sr-1817?lang=eng

The live redirect is handled by `index.html` in the repository root.

## GitHub Pages setup

Configure GitHub Pages to deploy from:

- Branch: `main`
- Folder: `/` root

Because this repository is only a redirect page, publishing from the root is simpler than using `/docs`.

## Changing the redirect

To update the destination, replace the URL in all three places in `index.html`:

- The `<meta http-equiv="refresh">` tag
- The `window.location.replace(...)` script
- The fallback `<a href="...">` link

Commit and push the change to the branch that GitHub Pages is publishing.

## Version branches

If you want easy rollback or staging, create branches with different `index.html` targets, for example:

- `redirect-whiteley`
- `redirect-next`
- `redirect-archive`

To promote a version, change the GitHub Pages publishing source to that branch and keep the folder set to `/` root.
