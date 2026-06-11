# RunCabin MCP server

Give your AI assistant the power to put real websites online. RunCabin is a **remote
(hosted) MCP server** - nothing to install or run locally; this repository documents it.

| | |
|---|---|
| **Server URL** | `https://runcabin.com/mcp` (Streamable HTTP) |
| **Auth** | OAuth 2.1 - your client opens a browser sign-in on first connect (no API key to paste) |
| **Official MCP Registry** | `com.runcabin/cabin` |
| **Docs, tool reference, troubleshooting** | https://runcabin.com/connect |

## What it does

- **A live URL in one tool call** - deploys a site to a free `*.sites.runcabin.com`
  subdomain over HTTPS. No DNS wait, no certificate wait, no payment.
- **A real domain when you're ready** - checks availability and price for free, then
  hands the human a checkout link. Custom-domain hosting is $19.99/mo.
- **The AI never spends your money** - anything paid happens on RunCabin's own
  checkout page, reviewed and approved by the human. Tools only ever return links.

## Tools

| Tool | What it does |
|---|---|
| `cabin_create_site` | Create a site from HTML/content |
| `cabin_deploy` | Deploy/update a site (returns the live URL) |
| `cabin_deploy_status` | Check a deployment's status |
| `cabin_list_sites` | List your sites |
| `cabin_check_domain` | Domain availability + price (free) |
| `cabin_attach_domain` | Start custom-domain attach (returns a human checkout link) |
| `cabin_domain_status` | Custom-domain provisioning status |

## Connect

**Claude (claude.ai / Desktop):** Customize → Connectors → Add custom connector →
`https://runcabin.com/mcp` → sign in. ([Step-by-step](https://runcabin.com/connect))

**Claude Code**
```bash
claude mcp add --transport http runcabin https://runcabin.com/mcp
```

**Cursor / VS Code / Windsurf** - add a remote MCP server with URL
`https://runcabin.com/mcp` (each tool opens the browser sign-in on first use).
Full per-tool instructions: https://runcabin.com/connect

## Notes

- The hosted service's source is not in this repository; this repo is the public
  documentation and listing home for the remote server.
- Privacy: https://runcabin.com/privacy.html · Terms: https://runcabin.com/terms.html
- Questions: ryan@runcabin.com
