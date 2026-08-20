---
name: coren_pr_cadastro-mcp
description: Skill da REST API do Conselho Regional de Enfermagem PR: Cadastro na MCP.AI: 1 endpoint em /api/coren_pr_cadastro. Conselho Regional de Enfermagem PR: Cadastro, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# Conselho Regional de Enfermagem PR: Cadastro — REST API skill

Você tem acesso à **Conselho Regional de Enfermagem PR: Cadastro** REST API na MCP.AI.

> Conselho Regional de Enfermagem PR: Cadastro, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/coren_pr_cadastro
```

Todo endpoint é um **POST** na Base URL + o path abaixo. Os parâmetros vão no corpo JSON.

## Autenticação

Inclua em toda request:

```
Authorization: Bearer sk_live_...
Content-Type: application/json
```

> Gere sua chave em **https://app.mcp.ai/settings/api-keys** (workspace API key `sk_live_…`, não expira, revogável). Uma única chave serve pra todos os seus MCPs.

## Formato de resposta

```json
{ "ok": true, "tool": "<tool_id>", "result": <payload> }
```

## Exemplo cURL

```bash
curl -X POST https://api.mcp.ai/api/coren_pr_cadastro/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{"categoria":"..."}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/coren_pr_cadastro/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `coren_pr_cadastro_consultar`

Conselho Regional de Enfermagem PR: Cadastro, consulta em fonte oficial. _(POST /api/coren_pr_cadastro/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `categoria` | string | Sim | Parâmetro de consulta "categoria". |
| `nome` | string | Não | Parâmetro de consulta "nome". |
| `registro` | string | Não | Parâmetro de consulta "registro". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_coren_pr_cadastro` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
