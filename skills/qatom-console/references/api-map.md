# Qatom API map for Console work

Generated 10 October 2026 from `https://pay.m.todaq.net/v4/openapi.json` (TODAQ Micro Payment API 4.0.0). The live document wins if they differ. Full reference: https://docs.m.todaq.net.

Only the endpoints that matter for running a store and a wallet are listed; sign-in, carts, embeds and notifications are left out.

## Wallets and twins

| Method | Path | What it does |
|---|---|---|
| GET | `/v4/dq` | List digital quantities |
| GET | `/v4/twin/dq` | List digital quantities |
| GET | `/v4/twin/{hostname}` | Get a twin |
| PUT | `/v4/twin/{hostname}` | Rename a twin |
| GET | `/v4/twin/{hostname}/binder` | Get a twin’s binder |
| POST | `/v4/twin/{hostname}/charge/complete` | Complete a card top-up |
| POST | `/v4/twin/{hostname}/charge/intent` | Start a card top-up |
| POST | `/v4/twin/{hostname}/charge/transfer` | Transfer a settled charge to a twin |
| GET | `/v4/twin/{hostname}/commodities` | List a twin’s commodities |
| POST | `/v4/twin/{hostname}/config` | Configure a twin’s paywall |
| GET | `/v4/twin/{hostname}/info` | Get twin node configuration |
| GET | `/v4/twin/{hostname}/inventory` | Export twin inventory |
| GET | `/v4/twins` | List your twins |
| POST | `/v4/user/accounts/{id}/twin` | Ensure the account has a twin |
| GET | `/v4/user/accounts/{id}/twins` | List an account's twins |
| POST | `/v4/user/accounts/{id}/twins` | Add a provider twin to an account |

## Records, verification and inventory

| Method | Path | What it does |
|---|---|---|
| GET | `/v4/catalog/purchases/{transaction_id}` | Look up a catalog sale |
| GET | `/v4/catalog/revenue` | Total revenue across your catalog |
| POST | `/v4/commodity` | Create a commodity |
| GET | `/v4/commodity/{hash}` | Get a commodity |
| PUT | `/v4/commodity/{hash}` | Update a commodity |
| GET | `/v4/commodity/{hash}/transactions` | List a commodity’s transactions |
| GET | `/v4/payment/{hash}/validate` | Look up a purchase validation |
| POST | `/v4/payment/{hash}/validate` | Redeem a purchase validation |

## Moving funds

| Method | Path | What it does |
|---|---|---|
| POST | `/v4/persona/delegate/{hash}/transfer` | Transfer under a delegate |
| POST | `/v4/transfer` | Transfer to a wallet or email address |

## Twin paywall and paying for services

| Method | Path | What it does |
|---|---|---|
| GET | `/v4/paywall` | Pay for and call a service (query form) |
| POST | `/v4/paywall` | Pay for and call a service |
| DELETE | `/v4/paywall/authorizations` | Revoke an authorization |
| GET | `/v4/paywall/authorizations` | List payment authorizations |
| PUT | `/v4/paywall/authorizations` | Approve or deny an authorization |
| GET | `/v4/paywall/preauthorization` | List spending budgets |
| POST | `/v4/paywall/preauthorization` | Set a spending budget for a service |
| DELETE | `/v4/paywall/preauthorization/{id}` | Revoke a spending budget |

## Approvals and spending limits

| Method | Path | What it does |
|---|---|---|
| GET | `/v4/agent/account` | The account this connection reads |
| POST | `/v4/agent/account-changes` | Make an approved change to the business account |
| POST | `/v4/agent/account-changes/spend` | Spend an approved account change made elsewhere |
| POST | `/v4/agent/account-choices` | Ask the user to choose the account this connection reads |
| GET | `/v4/agent/account-choices/{id}` | An account-choice request, and the accounts to choose from |
| POST | `/v4/agent/account-choices/{id}` | Choose the account |
| GET | `/v4/agent/account-choices/{id}/choose` | The account-choice page |
| POST | `/v4/agent/approvals` | Ask the user to approve a purchase, a cart, a top-up or an account change |
| GET | `/v4/agent/approvals/{id}` | Where an approval request stands |
| POST | `/v4/agent/approvals/{id}/decision` | Approve or decline an agent's request |
| GET | `/v4/agent/approvals/{id}/review` | The approval page |
| GET | `/v4/user/agent-approvals/settings` | Your auto-approve limit |
| PUT | `/v4/user/agent-approvals/settings` | Set your auto-approve limit |

## Delegated authority (personas and delegates)

| Method | Path | What it does |
|---|---|---|
| POST | `/v4/persona` | Create a persona |
| GET | `/v4/persona/delegate/{hash}` | Get a delegate |
| POST | `/v4/persona/delegate/{hash}` | Issue a delegate |
| GET | `/v4/persona/delegates` | List your delegates |
| GET | `/v4/persona/{hash}` | Get a persona |
| GET | `/v4/persona/{hash}/delegate` | Get a delegate |
| POST | `/v4/persona/{hash}/delegate` | Issue a delegate for a persona |
| PUT | `/v4/persona/{hash}/verify` | Verify a persona |

## Catalog items

| Method | Path | What it does |
|---|---|---|
| GET | `/v4/catalog/items` | List catalog items |
| POST | `/v4/catalog/items` | Create a catalog item |
| DELETE | `/v4/catalog/items/{id}` | Deactivate a catalog item |
| GET | `/v4/catalog/items/{id}` | Get a catalog item |
| PUT | `/v4/catalog/items/{id}` | Update a catalog item |
| GET | `/v4/catalog/items/{id}/dispatch-params` | List a catalog item's dispatch parameters |
| PUT | `/v4/catalog/items/{id}/dispatch-params` | Replace a catalog item's dispatch parameters |

## Accounts, users and MCP servers

| Method | Path | What it does |
|---|---|---|
| GET | `/v4/account` | Get your account |
| POST | `/v4/account` | Create an account |
| PUT | `/v4/account` | Update your account |
| DELETE | `/v4/mcp/servers/{hostname}/agent` | Detach the managed agent |
| GET | `/v4/mcp/servers/{hostname}/agent` | Get the managed agent |
| POST | `/v4/mcp/servers/{hostname}/agent` | Attach a managed agent |
| PUT | `/v4/mcp/servers/{hostname}/agent` | Update the managed agent |
| GET | `/v4/user` | Get a user |
| POST | `/v4/user` | Create a user |
| PUT | `/v4/user` | Update a user |
| GET | `/v4/user/accounts` | List the accounts you belong to |
| POST | `/v4/user/accounts` | Create an account you own |
| GET | `/v4/user/accounts/{id}` | Get an account you belong to |
| PUT | `/v4/user/accounts/{id}` | Update an account you belong to |
| GET | `/v4/user/accounts/{id}/mcp-servers` | List an account's managed MCP servers |
| GET | `/v4/user/accounts/{id}/secrets` | Get an account's secrets |
| GET | `/v4/user/accounts/{id}/users` | List an account's users |
