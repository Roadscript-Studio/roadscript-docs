# Roadscript™ Infrastructure
## Techical Setup
Domain name in mind: https://roadscript.studio  
Cloudflare is the single source of truth for DNS, TLS, and edge security

### Planned Setup:
- SSL: Let's Encrypt (Cloudflare)
- DNS + CDN: Cloudflare DNS
- Hosting: Cloudflare Pages
- Email: Proton Mail (@roadscript.studio)

### Custom Email Structure
- Maintain export access (IMAP/Bridge) or backup strategy for email in case of provider change.
- **Never publish admin@ on public pages**
- Public:
    1. contact@roadscript.studio: public contact email address
    2. developer@roadscript.studio: product development & engineering emails
    3. store@roadscript.studio: Etsy store emails
    4. legal@roadscript.studio: legal & trademark (& IP correspondance) email
    5. billing@roadscript.studio: billing email
    6. support@roadscript.studio: customer service support email
    7. noreply@roadscript.studio: no reply email
- Private:
    1. admin@roadscript.studio: administration level emails

### Traffic Analysis (Cloudflare Web Analytics)
- Start with Cloudflare Web Analytics
- Re-evaluate Plausible or Simple Analytics if traffic or product complexity increases

### Security
- **turn on 2FA and domain registrar lock** 
- Store recovery codes for registrar, Cloudflare, and Proton in an offline password manager or secure archive

### Future upgrades:
1. Uptime monitor: UptimeRobot (free tier) / Better Stack (nice UI)
2. Minimum landing page (establish brand legitimacy)
  - About Roadscript
  - What is coming
  - Contact hello@roadscript.studio
  - Social media links
3. Subdomains
  - studio.roadscript.studio → photography application
  - store.roadscript.studio → Etsy store (redirect-only alias pointing to Etsy)
  - status.roadscript.studio → uptime page

---
