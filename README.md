# shopquotes-policies

Static public policy pages for ShopQuotes (operated by ShopTrade Pte Ltd), hosted on GitHub Pages at **policy.shopquotes.com**.

```
index.html          ->  https://policy.shopquotes.com/
privacy/index.html  ->  https://policy.shopquotes.com/privacy
terms/index.html    ->  https://policy.shopquotes.com/terms
CNAME               ->  custom domain for GitHub Pages
```

## Deploy (GitHub Pages)

1. Create a new **public** GitHub repo, e.g. `shopquotes-policies`, and push these files to the `main` branch.
   ```bash
   git init && git add . && git commit -m "ShopQuotes public policies"
   git branch -M main
   git remote add origin git@github.com:<org>/shopquotes-policies.git
   git push -u origin main
   ```
2. Repo **Settings -> Pages**: Source = Deploy from a branch, Branch = `main`, Folder = `/ (root)`.
3. **Custom domain**: it should already read `policy.shopquotes.com` from the `CNAME` file. If not, set it there.
4. **DNS** (at your domain's DNS provider): add a record
   ```
   CNAME   policy   <github-username-or-org>.github.io
   ```
5. Wait a few minutes for GitHub to issue the HTTPS certificate, then enable **Enforce HTTPS**.

## Use in Google OAuth consent screen

- Application home page:  `https://policy.shopquotes.com`
- Privacy policy link:    `https://policy.shopquotes.com/privacy`
- Terms of service link:  `https://policy.shopquotes.com/terms`

## Notes

- The privacy policy includes Google's required **Limited Use** disclosure for Gmail data.
- These are practical templates. Have them reviewed before relying on them for legal compliance.
- Update the "Last updated" dates and the contact email (`support@shopquotes.com`) if needed.
