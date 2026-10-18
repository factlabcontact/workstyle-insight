# GitHub Pages migration

Site: https://workstyle-insight.tokyo/
Owner: factlabcontact
Repository: workstyle-insight

## Status

index.html preserves the pre-migration live article byte for byte. article-draft.html contains the proposed replacement and retains noindex until the owner verifies the biography, activity evidence, real testimonials and consent, operator details, and contact information. No testimonials have been invented.

Original index.html SHA-256: 5412852e077e5c114305364aed58048993dabdc8b04efed346dd606335088e91

## Hosting

Publish the main branch root through Settings > Pages. GitHub Pages serves the HTML; Cloudflare-specific _headers and Apache .htaccess files are not used.

## Custom domain cutover

1. Verify the domain in the GitHub account Pages settings.
2. Set workstyle-insight.tokyo as the repository Pages custom domain.
3. Update only the website DNS records using current GitHub Pages documentation. Preserve MX and TXT records used for email and verification.
4. Wait for DNS validation and certificate issuance, then enable Enforce HTTPS.
5. Check the domain returns HTML, Japanese text renders correctly, and contact links work before retiring the old Pages project.

Documentation: https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site

## Cutover changes

- GitHub Pages custom domain: workstyle-insight.tokyo
- GitHub account domain ownership: verified via DNS TXT
- Cloudflare Worker custom domain binding removed; Worker deployment retained for rollback
- Apex CNAME -> factlabcontact.github.io, DNS only
- www CNAME -> factlabcontact.github.io, DNS only
- Existing Google verification TXT retained
- Original content HTTP 200 and byte identity verified after cutover

If rollback is necessary, remove the apex CNAME and reattach workstyle-insight.tokyo under the retained Cloudflare Worker workstyle-insight > Domains > Add Domain. Verify DNS and HTTPS after any rollback.
