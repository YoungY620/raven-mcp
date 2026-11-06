# Raven

Raven lets an assistant search a financial institution's proprietary research library and run AI investment research with the signed-in user's own Raven account.

The only public MCP endpoint is:

```text
https://research-agent.ss-relay-yangyi.workers.dev/agent/mcp
```

## Connect

In Grok, add a custom connector with that URL. In Cursor, install this plugin or add the same URL as a remote MCP server. The client signs in with OAuth. Do not paste an API key, cookie, or bearer token.

After login, enable the modules this client should use in the Raven console. Modules start disabled. Enabling one exposes it to authorized connections for that account.

## Review check

1. Add `https://research-agent.ss-relay-yangyi.workers.dev/agent/mcp`.
2. Complete the Raven sign-in. Use an account that can open this deployment.
3. Enable the knowledge and research modules for that account.
4. Ask: "Search the proprietary library for the latest note on the covered company and quote the source."
5. The answer should come from that account's Raven library and name the source document. A web summary without a library source is not a pass.
