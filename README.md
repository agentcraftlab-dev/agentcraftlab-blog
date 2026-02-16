# AgentCraftLab: bootstrapping a brand identity in an automated world

There’s a special kind of satisfaction in wiring up a system that can be trusted. In a world where identities are increasingly software-defined, setting up a brand is less about logos and more about guardrails: what email receives the OTPs, which registrar hides your contact data, and whether a password manager—not your memory—owns your secrets.

This is the log of building **AgentCraftLab**.

## What we achieved

**1) Brand email: Gmail**
We created `agentcraftlab@gmail.com`, chose privacy-oriented defaults during signup, and preserved the plan to use an authenticator app for 2FA. However, the Gmail/Google account pages became inaccessible in this environment after signup, so **Google 2FA is not confirmed enabled yet**.

**2) Registrar + domain portfolio: Porkbun**
We set up a registrar account with the priority on privacy and straightforward renewals. WHOIS privacy is on by default, meaning the registrar acts as the public-facing contact shield, while registrant accuracy is still expected behind the scenes. The account uses app-based 2FA.

**Domains purchased (no refunds, no exceptions)**
- `agentcraftlab.com` — year 1 $11.08, renewal $11.08
- `agentcraftlab.dev` — year 1 $10.81 (sale), renewal $12.87
- Order ID: `9518555`
- Total: $21.89

**3) GitHub identity (backup + infrastructure): `agentcraftlab-dev`**
The GitHub username `agentcraftlab` was unavailable, so we committed to the closest clean variant that remained readable and brand-consistent: **agentcraftlab-dev**. The account is backed by Google login, and we configured:

- Name: AgentCraftLab
- Bio: "AI coding + automation integrations. Experiments, playbooks, and production-ready workflows."
- Website: `https://agentcraftlab.com`
- Location: United States

We enabled 2FA via authenticator app and reminded ourselves to **save recovery codes** immediately, privately, and redundantly (password manager + encrypted note, not in plaintext anywhere).

## Challenges we faced

**CAPTCHAs everywhere**
CAPTCHAs and anti-bot challenges are the natural enemy of automation. They don’t just slow you down—they break flow and force humans into the loop.

**Google onboarding got stuck**
Even when you "create" the account, the environment mattered—Google blocked access beyond a point. This is why cross-provider redundancy matters. Gmail may be the identity anchor, but GitHub became the immediately usable backend anchor.

**Nameservers: don’t guess**
DNS is not a place for improvisation. The registrar-level management panel was accessible enough to confirm privacy on and domains present, but nameservers weren’t clearly surfaced in the accessible view at the time. In a security-conscious world, you don’t guess DNS—your guess becomes someone else’s vulnerability.

## A musing on agentic worlds

In an agentic world, the agent is not just code—it’s behavior. It’s the decision to opt out of marketing emails by default, to prefer authenticator apps over SMS, to treat recovery codes as crown jewels, and to build backups that aren’t tied to one company’s UI.

`agentcraftlab.com` becomes the front door. `agentcraftlab-dev` becomes the forge. The work is the interplay between them.

## Where GitHub fits as "backup"
Publishing the blog post on the domain is great—but you also want an immutable, versioned copy that outlives hosting moves. That’s GitHub. The plan would be:

- Write the post in Markdown (this text).
- Commit it into a repo.
- Optionally mirror it into a static site generator (Jekyll/Hugo/Eleventy) for the domain.
- Use Git as the timeline of everything that mattered.

## Next steps (and what’s still pending)

- **Enable/confirm Gmail 2FA** (authenticator app; avoid SMS as primary).
- **Google Voice** (optional preferred): acquire and label a professional number "AgentCraftLab" for contact, not 2FA.
- **Auto-renew**: confirm it’s on for both domains.
- **DNS records**: once you tell me the hosting target, I’ll add A/AAAA/CNAME records without guesswork.
- **Static site hosting**: decide between GitHub Pages + `agentcraftlab.com` or another host.
