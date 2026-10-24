# AgentTwin agent tools

Official public integration resources for [AgentTwin agent testing](https://agenttwin.si/).
The product implementation repository is private; this repository contains only
public agent instructions, two skills and read-only documentation MCP configuration.

## Skills

- **agenttwin-prepare** — prepare a real repository workflow with explicit invocation,
  synthetic fixtures, supported operations and correctness assertions.
- **agenttwin-investigate** — investigate recorded failures and verify an application
  repair against unchanged checks.

Install both with a compatible skills client:

```sh
npx skills add Sashank-Singh/agenttwin-agent-tools
```

Review the skills before installing. This does not install the CLI or run application
code. The [AgentTwin Node CLI](https://www.npmjs.com/package/agenttwin) is separate.

## Agent configuration

`AGENTS.md` gives coding agents public integration guidance. Cursor users can opt
into `.cursor/rules/agenttwin.mdc`. The portable Agent Plugins manifest is
`plugin.json`, with the documentation server configured in `mcp.json`. Use your
client's supported plugin installer; client support varies.

The public MCP at `https://agenttwin.si/mcp/docs` supplies `search_docs` and
`read_doc`. No credentials are required. It has no customer access or execution.
The [official MCP Registry entry](https://registry.modelcontextprotocol.io/?q=io.github.Sashank-Singh%2Fagenttwin-docs)
links to the owned developer page and endpoint.

## Maintained references

- [Developer portal](https://agenttwin.si/developers/)
- [OpenAPI](https://agenttwin.si/openapi.json)
- [API authentication](https://agenttwin.si/auth.md)
- [World preparation](https://agenttwin.si/docs/preparation.md)
- [Operation contracts](https://agenttwin.si/docs/provider-operations.md)
- [Synthetic sandbox](https://agenttwin.si/sandbox/)
- [API versioning and deprecation](https://agenttwin.si/api-policy/)

Local workflow execution can access the host filesystem and network. Review code,
fixtures and invocation before running. Static discovery is not a runnable test;
no production replica, provider parity or automatic repair is promised.

The canonical maintained source for these public files lives in AgentTwin's
website integration bundle. MIT licensed; see LICENSE.
