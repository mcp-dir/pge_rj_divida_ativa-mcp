---
name: pge_rj_divida_ativa-mcp
description: Skill da REST API do Procuradoria Geral do Estado RJ: Dívida Ativa na MCP.AI: 1 endpoint em /api/pge_rj_divida_ativa. Procuradoria Geral do Estado RJ: Dívida Ativa, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# Procuradoria Geral do Estado RJ: Dívida Ativa — REST API skill

Você tem acesso à **Procuradoria Geral do Estado RJ: Dívida Ativa** REST API na MCP.AI.

> Procuradoria Geral do Estado RJ: Dívida Ativa, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/pge_rj_divida_ativa
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
curl -X POST https://api.mcp.ai/api/pge_rj_divida_ativa/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/pge_rj_divida_ativa/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `pge_rj_divida_ativa_consultar`

Procuradoria Geral do Estado RJ: Dívida Ativa, consulta em fonte oficial. _(POST /api/pge_rj_divida_ativa/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `renavam` | string | Não | Parâmetro de consulta "renavam". |
| `cnpj` | string | Não | Parâmetro de consulta "cnpj". |
| `cpf` | string | Não | Parâmetro de consulta "cpf". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_pge_rj_divida_ativa` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
