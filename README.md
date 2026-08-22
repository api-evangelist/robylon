# Robylon AI (robylon)

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

Enterprise AI customer-support platform across voice, WhatsApp, chat, email, social media and
ticketing. AI agents run against a customer knowledge base with configurable personas, model
selection, human handover and assignment logic; the APIs let external systems interact with
Robylon and trigger workflows including voice and outbound automation.

**APIs.json:** [apis.yml](https://raw.githubusercontent.com/api-evangelist/robylon/refs/heads/main/apis.yml)

- **Website:** https://www.robylon.ai
- **Documentation:** https://guides.robylon.ai/
- **llms.txt:** https://guides.robylon.ai/llms.txt
- **MCP:** https://guides.robylon.ai/mcp

Part of the [API Evangelist](https://apievangelist.com) network.

## How this entry was built

Added on request from Robylon's growth team, who asked to be indexed and offered to supply whatever
artifacts would help. Everything here is harvested from the live surface on 2026-08-20; nothing is
derived or modelled.

The documentation is public, extensive, and served to everyone — every request was run twice, with
a default client user-agent and with a browser user-agent, and the bytes are identical. Robylon
filters nobody, which is worth stating because a good number of providers do.

**No machine-readable contract.** No OpenAPI or apis.json is served on either host. The obvious
paths and the docs-platform conventions were both probed — `/openapi.json`,
`/references/openapi.yaml`, `/openapi/api-reference.json`, `/api-reference/introduction` — all 404.
The single API entry therefore asserts no operations, because none are readable.

**The MCP server is a docs server.** It is real and unauthenticated, and it is emitted by the
Mintlify docs platform: its tools search the documentation corpus. None of them create a ticket,
place a call, or trigger a workflow. An agent can learn how to integrate Robylon through MCP but
cannot transact with it.

**One defect worth reporting back.** The MCP descriptor at `/.well-known/mcp.json` advertises
`https://robylonai.main-kill-isr.mintlify.me/mcp`, a Mintlify preview hostname, while the endpoint
actually answers at `guides.robylon.ai/mcp`. An agent following the descriptor is pinned to a vendor
preview host Robylon does not control.
