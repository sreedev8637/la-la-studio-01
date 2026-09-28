# The Lala Studio — GitHub Pages export

This folder contains the complete static website. There is no build step.

## Publish later

1. Create a GitHub repository. Upload all files from this folder to the **root** of its default branch, including `index.html` and `.nojekyll`.
2. In repository **Settings → Pages**, choose **Deploy from a branch**, the default branch, and **/(root)**. Save.
3. When ready to use your domain, enter it under **Settings → Pages → Custom domain** and configure DNS according to GitHub's instructions. GitHub will add `CNAME` for branch publishing. Enable HTTPS once offered.
4. Once the final public address works, add its absolute URL to the HTML as `rel="canonical"`, Open Graph `og:url`, and the `url` property of the `BeautySalon` JSON-LD. Add a `sitemap.xml` containing that address, and include `Sitemap: https://YOUR-DOMAIN/sitemap.xml` in `robots.txt`. Do not reuse the private preview URL.

## Instagram posts

The page reads the published Google Sheet supplied for the Instagram posts, with a second public-sheet method and `instagram-posts.csv` fallback. Keep column A headed `url`, with one public Instagram post or reel URL per row. The browser may block Google's CSV endpoint; check a changed post on the live Pages URL. If updates are not reflected, the gallery displays the bundled fallback until a compatible sheet endpoint or sync is added.

## Site files

Keep the images, icons, service price PDF, CSV and HTML together at repository root; the page uses relative paths. The private Sites preview is independent of this export.
