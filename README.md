# metalbuildings.pro: Coming soon

A responsive, self-contained coming soon page. All copy and styling live in `index.html`. No dependencies, external fonts, JavaScript, or build step are required.

## Preview

Open `index.html` in your browser, or run `python -m http.server 4173 --bind 127.0.0.1` from this folder and visit http://127.0.0.1:4173.

## Publish on GitHub Pages

The Git remote is `https://github.com/TDodgeCo/metalbuildings-pro-coming-soon.git`.

1. In the GitHub repository, open **Settings → Pages**.
2. Under **Build and deployment**, set **Source** to **GitHub Actions**.
3. Commit the site files and `.github/workflows/deploy-pages.yml`, then push to `main`.
4. The **Deploy to GitHub Pages** workflow will publish the page automatically. Future pushes to `main` will update it. You can also run the workflow manually from the **Actions** tab on `main`.
5. Wait for the workflow to finish; its deployment environment will link to the published site.

The workflow publishes only `index.html` and `.nojekyll`. Documentation and repository files are excluded from the site artifact.

These steps follow [GitHub's publishing-source documentation](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site). To use metalbuildings.pro as the live address, configure the custom domain and DNS separately using [GitHub's custom-domain guide](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site).

GitHub Pages is configured to publish this repository through GitHub Actions with `metalbuildings.pro` as the custom domain. The initial deployment completed on October 2, 2026.

## Domain configuration

DNS is hosted on Porkbun's existing authoritative nameservers. The zone was empty when configured. Its new records are:

| Type | Host | Value | TTL |
| --- | --- | --- | --- |
| A | @ | 185.199.108.153 | 600 |
| A | @ | 185.199.109.153 | 600 |
| A | @ | 185.199.110.153 | 600 |
| A | @ | 185.199.111.153 | 600 |
| CNAME | www | tdodgeco.github.io | 600 |

There are no email or previous provider records in this configuration. GitHub manages the HTTPS certificate. Its issuance and HTTPS enforcement status can be checked in **Settings → Pages**.

## Edit

Edit the text in `index.html`. Colors are defined in the `:root` CSS variables near the top. Contact links use `mailto:` and `tel:` so visitors can open their email or phone app.

## Verification

Checked in a browser at desktop (1440 × 1200) and mobile (390 × 844) sizes: content, heading hierarchy, layout, and contact link destinations. Neither viewport had horizontal overflow. Email and telephone destinations were verified without sending an email or placing a call.
