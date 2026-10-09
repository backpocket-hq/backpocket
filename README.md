# Backpocket

Electrical-contractor marketing page, version 6. Six workflow use cases, an example pay-app check, a value calculator, and a prefilled email handoff.

## Publish

In Settings → Pages, select Deploy from a branch, main, and /(root). Save. No build or dependencies are required.

Keep the noindex tags during review. Demonstration data is fictional; the page does not connect to accounting systems. The form posts to FormSubmit, which emails each request to the Backpocket team. The first submission sends a one-time confirmation email that the inbox owner must click.

## Editing together

Make changes on a branch and open a pull request before merging into main. Once Pages is enabled, main is the published site. Invite Jon using his verified GitHub username through repository access settings.

## Assets

Electrical-work photo: Pexels photo 34054464, attributed on the page.

## Versions

- `/` is v6, the page Brad published first.
- `/v2/` is the redesigned page (back-office agent, photo hero, job switcher). It lives in its own folder, so v6 stays untouched. On Pages it is at `/backpocket/v2/`.

## Keeping the pages out of search and scrapers

- Both pages carry `noindex, nofollow, noarchive, nosnippet, noimageindex` and `noai, noimageai` meta tags.
- `robots.txt` disallows all crawlers and the common AI scrapers. Crawlers only read it from the domain root, so copy it into a repo named `backpocket-hq.github.io` (an organization owner creates that repo).
- These are requests, not locks. Anyone with a link can open the page, and a scraper can ignore the rules. Real access control needs a password or login in front of the site.

## Custom domain

The `CNAME` file sets the Pages custom domain to `getbackpocketai.com`. Do not delete it. DNS lives at Namecheap: four A records on the root pointing to GitHub Pages (185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153) and a CNAME for `www` pointing to `backpocket-hq.github.io`. Keep the Google MX, SPF, DKIM, and verification records on the same domain untouched.

## Versions on the site

- `/` is v9, the current page (copy of `/v2/`).
- `/v2/` is v9 at its earlier address. Keep it so links already sent still work.
- `/v1/` is the old v6 page. Kept for reference. Delete when Jon and Brad agree.

## Form

The form posts to FormSubmit, which emails `hello@getbackpocketai.com`. The first submission sends a one-time activation email to that inbox. Click the link in it once. Make sure `hello@` exists as a mailbox or alias first.
