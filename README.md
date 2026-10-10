# Minds Beyond

Static one-page site for Minds Beyond, served at [mindsbeyond.si](https://mindsbeyond.si).

- `index.html`: the whole site, with inline CSS. No build step.
- `favicon.svg`: the logo mark.
- `CNAME`: the custom domain.

Edit `index.html` and push to `main`. The workflow in `.github/workflows/pages.yaml` publishes it.

## GitHub Pages

Repo: `mindsbeyond/mindsbeyond.github.io` (public).

1. Settings > Pages > Build and deployment > Source: **GitHub Actions**.
2. Custom domain: `mindsbeyond.si`.
3. Tick **Enforce HTTPS** once DNS resolves and the certificate is issued.

Optional: verify the domain under your GitHub account (or org) settings > Pages. This adds one TXT record and stops anyone else from claiming the domain.

## DNS (Regery)

| Type  | Host  | Value                   |
|-------|-------|-------------------------|
| A     | `@`   | `185.199.108.153`       |
| A     | `@`   | `185.199.109.153`       |
| A     | `@`   | `185.199.110.153`       |
| A     | `@`   | `185.199.111.153`       |
| CNAME | `www` | `mindsbeyond.github.io` |

Check with:

```sh
dig +short mindsbeyond.si A
dig +short www.mindsbeyond.si
```
