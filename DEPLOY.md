# Deploy krypt.abrdns.com (free, about 15 minutes)

## Option A: GitHub Pages (recommended)
1. Create a free GitHub account, then a **public** repository named `krypt-site`.
2. Upload everything in this folder to the repository root: `index.html`, `og.png`, `favicon.svg`, `CNAME`, `.nojekyll`, `robots.txt`.
3. Repository **Settings → Pages**: Source = *Deploy from a branch*, Branch = `main`, folder `/ (root)`. Under *Custom domain* enter `krypt.abrdns.com` and save.
4. In **ClouDNS**, open the DNS zone for `krypt.abrdns.com` and add four **A** records with an empty host (the apex), TTL default:
   - 185.199.108.153
   - 185.199.109.153
   - 185.199.110.153
   - 185.199.111.153
   Optional IPv6 (**AAAA**, empty host): 2606:50c0:8000::153, 2606:50c0:8001::153, 2606:50c0:8002::153, 2606:50c0:8003::153.
   Delete any other A or CNAME record on that same host. If ClouDNS shows `krypt` as a host inside the `abrdns.com` zone instead, use host `krypt`.
5. DNS can take up to 24 hours. Then tick **Enforce HTTPS** in Settings → Pages (it can take a while to appear).
6. Test on your phone: open https://krypt.abrdns.com, tap FR/EN, tap both buttons.

## Option B: Netlify drag and drop (no GitHub)
Drop this folder on app.netlify.com/drop, add `krypt.abrdns.com` as a custom domain, and create exactly the DNS record Netlify displays.

## Notes
- GitHub's IP addresses are from GitHub's own documentation (checked 8 Oct 2026).
- Cloudflare cannot take `abrdns.com` subdomains yet (reported 5 Oct 2026), so do not move DNS there.
- Free shared subdomains can be treated with suspicion by Facebook. Post the link early to test; a cheap own domain (about $5–10 a year) is the fallback.
- WhatsApp group: in group settings turn on "Approve new participants" because the invite link is public.
- Before launch, confirm each statement on the page against hfm.com, and swap in a French HFM link from myHF if one exists (the current link opens HFM's English page).
