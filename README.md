# AgentifAI

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

AgentifAI is a Portuguese enterprise conversational-AI company, headquartered in Braga and
operating across the EU, that builds **AliceOS** — a voice-first AI contact-center and autonomous
agent platform purpose-built for the regulated banking and healthcare sectors. AliceOS orchestrates
multi-agent workflows across phone, WhatsApp, SMS, email and web channels, integrates with core
banking systems, CRMs, fraud engines, Hospital Information Systems and EMR/EHR platforms over REST,
SOAP and OAuth, and connects to telephony through SIP trunking and CTI adapters. Reference
deployments include Santander, Banco BPI, Caixa Geral de Depositos, Vivalto Sante, Lusiadas Saude,
Ribera Salud and Luz Saude.

## What this profile found

AgentifAI sells a **managed enterprise deployment**, not a self-serve developer product, and its
public surface reflects that. It publishes real, first-party machine-readable and trust material:

- **`llms.txt`** — a genuine first-party llms.txt at <https://www.agentifai.com/llms.txt>, saved
  verbatim to [`llms/agentifai-llms.txt`](llms/agentifai-llms.txt), plus an `llms-full.txt`
  companion.
- **A SafeBase trust center** at <https://trust.agentifai.com/> naming SOC 2 Type 2,
  ISO/IEC 27001, ISO/IEC 42001:2023, PCI DSS v4.0.0 and HIPAA, with subprocessors and a
  Responsible Disclosure policy — see [`security/`](security/) and
  [`conformance/`](conformance/).
- **A solid domain-security posture** — TLS 1.3, HSTS with a one-year max-age, CAA, SPF and a
  DMARC `quarantine` policy (no DNSSEC) — see
  [`security/agentifai-domain-security.yml`](security/agentifai-domain-security.yml).

It publishes **no public API contract**. There is no developer portal, no API reference, no
OpenAPI/AsyncAPI/GraphQL surface, no MCP server and no A2A agent card. No `docs.`, `api.`,
`developer.` or `app.` subdomain resolves in DNS, every `/.well-known/` path on a host the company
controls returns `404`, and the only route to the platform published anywhere is the
<https://www.agentifai.com/talk-to-us> enterprise-demo form. The company markets "Enterprise API
Integration" and "Custom Digital Channels via REST APIs" as AliceOS capabilities, so an API almost
certainly exists behind the engagement — it is simply not published.

### Two name collisions this profile deliberately rejected

Recorded in [`packages/agentifai-packages.yml`](packages/agentifai-packages.yml) so a later run
does not adopt them:

- The npm scope **`@agentifai-oss/*`** resolves to `github.com/Lelianto/agentifai`, an
  individual's personal monorepo. Not first-party.
- The GitHub org **`agentifai-ai`** is a **different company** — its own metadata names
  `agentifai.ai` and the United Arab Emirates. The org `Agentifai` is an empty 2023 placeholder
  with zero repositories.

Likewise, the RFC 9727 `api-catalog` served at `careers.agentifai.com/.well-known/api-catalog` is
generated by **Teamtailor** for every one of its tenants — it is a vendor surface running under an
AgentifAI subdomain, and is recorded but not credited.
