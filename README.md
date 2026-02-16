# AgentCraftLab: bootstrapping a brand identity in an automated world

This log is about building guardrails first: privacy defaults, 2FA everywhere, and keeping deployment lightweight so you can move fast without leaking secrets.

## What we achieved

**1) Brand email (Gmail)**  
Brand account created with privacy-oriented defaults; plan remains to use an authenticator app for 2FA. (Google 2FA not confirmed enabled yet.)

**2) Registrar + domain portfolio (Porkbun)**  
Account configured with WHOIS privacy. Domains purchased (prices shown at checkout):
- `agentcraftlab.com` — year 1 $11.08; renewal $11.08
- `agentcraftlab.dev` — year 1 $10.81 (sale shown at checkout); renewal $12.87  
Total: $21.89 (no refunds stated at checkout)

**3) GitHub identity (backup + infrastructure)**  
GitHub account: `agentcraftlab-dev` (authenticator-based 2FA enabled). Profile configured with minimal public info.

**4) Work showcase / blog**  
Repo: `agentcraftlab-dev/agentcraftlab-blog`
- GitHub Pages hosting enabled
- Custom domain saved: `agentcraftlab.com`
- DNS configured for GitHub Pages: apex A records + `www` CNAME (kept as technical notes in the repo)
- `/blog` + `/work` route conventions planned for a clean static site expansion

## Challenges (honest notes)
- CAPTCHAs and OTP verification added unavoidable human steps.
- DNS and HTTPS require patience: propagation + certificate issuance can take time.
- Privacy discipline means you don’t publish transaction details or contact info—ever.
