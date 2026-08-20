# Robylon AI (robylon)

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
