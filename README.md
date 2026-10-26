# Omer Oztan Portfolio

A standalone, static portfolio page for publishing at `oztanomer.com` with GitHub Pages. It has no build step or runtime dependencies.

## Preview locally

From the project root:

```sh
python3 -m http.server 8080 --directory portfolio-site
```

Open <http://localhost:8080>.

## Publish with GitHub Pages

Use a separate **public** repository named `omeroztan.github.io` so the portfolio can deploy independently of the assistant application. Copy the contents of this directory into that repository's root, push to `main`, then in **Settings → Pages** choose **Deploy from a branch**, select `main` and `/ (root)`. GitHub Pages on the Free plan requires a public repository.

The included `CNAME` file sets the intended custom domain to `oztanomer.com`. In the Pages settings, confirm that custom domain. At your domain's DNS provider, point the apex domain to the GitHub Pages addresses listed in GitHub's custom-domain instructions. Keep the assistant's separate subdomain DNS record pointed at the VPS.

The portfolio is static; it does not need the assistant's VPS, Docker services, Firebase credentials, or application `.env` files.
