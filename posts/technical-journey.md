# Technical appendix: AgentCraftLab infrastructure

This appendix documents the technical decisions that make the brand identity secure, low-cost, and easy to deploy—without exposing sensitive personal information.

## GitHub Pages hosting
- Repo: `agentcraftlab-dev/agentcraftlab-blog`
- Pages build: `main` branch, root folder
- Default Pages URL: `https://agentcraftlab-dev.github.io/agentcraftlab-blog/`
- Custom domain configured: `agentcraftlab.com`

## DNS configuration (GitHub Pages)
We configured the registrar-managed DNS so the apex and `www` point to GitHub Pages.

### Apex (agentcraftlab.com)
- `A` → `185.199.108.153`
- `A` → `185.199.109.153`
- `A` → `185.199.110.153`
- `A` → `185.199.111.153`

### www
- `CNAME` for `www` → `agentcraftlab-dev.github.io`

### Mail forwarding
- Existing MX + SPF/TXT records were kept intact so email forwarding doesn’t break.

## .dev handling (privacy + cost)
`agentcraftlab.dev` is set to redirect to `https://agentcraftlab.com/` using:
- 301 permanent redirect
- wildcard redirect (subdomains follow)
- “include path” enabled (URLs under `.dev` carry through)

## Security defaults
- Registrars/services use privacy/WHOIS shields where offered.
- Primary 2FA preference is authenticator app (not SMS).
- Recovery codes/secrets are stored privately (not in the repo).
