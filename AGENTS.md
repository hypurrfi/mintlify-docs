# HypurrFi Documentation Project

## About

This is the documentation site for [HypurrFi](https://hypurr.fi), built on [Mintlify](https://mintlify.com). HypurrFi builds lending, credit, and infrastructure products on Hyperliquid EVM (HyperEVM).

For full protocol context, integration patterns, and help bot instructions, see **`SKILL.md`** in this repo root.

## Content Structure

The docs are organized into four tabs in `docs.json`:

- **For Humans** — user-facing tutorials, product explainers, how-to guides. Written in second person with Mintlify components (Steps, Notes, Accordions).
- **For Agents** — agent-readable protocol references. Dense, code-first, self-contained. No Mintlify UI components.
- **For Developers** — technical references: smart contract APIs, integration guides, contract addresses.
- **AI Tools** — setup instructions for AI coding agents (Cursor, Claude Code, Windsurf).

## Terminology (Critical)

- **HypurrFi Prime** — isolated lending markets (Euler V2), one risk profile
- **HypurrFi Yield** — isolated lending markets (Euler V2), different risk profile. NOT earn vaults.
- **HypurrFi Markets** — umbrella name for Prime + Yield (the Euler V2 stack)
- **Earn Vaults** — curated managed strategies routing deposits to Prime/Yield markets. Separate product from Prime/Yield.
- **Pooled Markets** — shared-pool lending (Aave V3.0.2). Do not call it "Aave."
- **Legacy Markets** — deprecated Fraxlend-based isolated markets. Repay and withdraw only.
- **Mewler** — community name for HypurrFi Markets. Acceptable in casual references.
- **USDXL** — CDP-hybrid synthetic dollar. **NEVER call it a "stablecoin."** This is a compliance requirement.
- **"Vault"** — In Euler terminology, every lending market is a "vault." Do not confuse with HypurrFi's "Earn Vaults" product.

## Style

- **For Humans pages**: active voice, second person ("you"), Mintlify components, step-by-step tutorials
- **For Agents pages**: code-first, flat structure, all addresses inline, self-contained, no UI components
- **For Developers pages**: technical accuracy, Solidity/TypeScript examples, API signatures
- Use sentence case for headings
- Bold for UI elements: Click **Settings**
- Code formatting for file names, commands, paths, and code references

## Local Development

```bash
source ~/.nvm/nvm.sh && nvm use 22 && npx mintlify dev --port 3000
```

Node 22 required (Node 25+ not supported by Mintlify).
