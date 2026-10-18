# GitHub Pages migration

Site: https://workstyle-insight.tokyo/
Owner: factlabcontact
Repository: workstyle-insight

## Status

The article is a draft. Keep the noindex meta until the owner has verified the biography, activity evidence, real testimonials and consent, operator details, and contact information. No testimonials have been invented.

## Hosting

Publish the main branch root through Settings > Pages. GitHub Pages serves the HTML; Cloudflare-specific _headers and Apache .htaccess files are not used.

## Custom domain cutover

1. Verify the domain in the GitHub account Pages settings.
2. Set workstyle-insight.tokyo as the repository Pages custom domain.
3. Update only the website DNS records using current GitHub Pages documentation. Preserve MX and TXT records used for email and verification.
4. Wait for DNS validation and certificate issuance, then enable Enforce HTTPS.
5. Check the domain returns HTML, Japanese text renders correctly, and contact links work before retiring the old Pages project.

Documentation: https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site
