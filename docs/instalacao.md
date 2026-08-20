# Instalação detalhada

Conselho Regional de Enfermagem PR: Cadastro é um servidor MCP remoto. Aponte seu cliente pra `https://api.mcp.ai/p_coren_pr_cadastro`. Snippets rápidos: [INSTALL.md](../INSTALL.md).

| Cliente | URL | Auth |
|---|---|---|
| Claude Desktop | `https://api.mcp.ai/p_coren_pr_cadastro` | OAuth 2.1 ou agent-auth |
| Cursor | `https://api.mcp.ai/p_coren_pr_cadastro` | OAuth 2.1 ou agent-auth |
| VS Code (Copilot) | `https://api.mcp.ai/p_coren_pr_cadastro` | OAuth 2.1 ou agent-auth |

A config JSON é a mesma em todos: só a URL, sem headers.

## Desinstalar

Remova o bloco `mcpServers.coren_pr_cadastro` (ou `servers.coren_pr_cadastro` no VS Code) do config do cliente e reinicie.
