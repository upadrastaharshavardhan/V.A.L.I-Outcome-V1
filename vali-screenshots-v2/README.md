# VALI Detailed Live Screenshots (Run 2)

Fully progressed session — **no forbidden pages** on progressive layers.

## Session unlock path completed

```
home → login → dashboard → users
  → API Docs (unlocked)
  → Staging (unlocked)
  → Config (unlocked)
  → Backups (unlocked)
  → Secrets Vault (unlocked)
```

Canary paths also hit (`/api/v1/secrets`, backup download).

## Attack simulation

| Tool signature | Behavior |
|----------------|----------|
| Chrome browser | Interactive progressive exploration |
| sqlmap | Injection-style probing |
| gobuster | Directory discovery |
| Nmap NSE | Scanner fingerprint |
| python-requests | Scripted access |

## Live intelligence (this run)

- Multiple sessions with high risk scores
- Tools: browser, dirbuster, scanner, script, sqlmap
- Kill-chain: recon, credential_access, discovery, collection, high_value, progress
- Canary hits recorded
- Profiles: targeted + automated

## Screenshot index

| File | Content |
|------|---------|
| 01-home.png | NexusOps Internal Administration Portal |
| 02-login.png | Administrator Sign In |
| 03-operations-dashboard.png | Operations Dashboard (metrics + activity) |
| 04-user-management.png | User directory table |
| 05-api-docs-unlocked.png | Internal API Reference (unlocked) |
| 06-staging-unlocked.png | Staging Control Panel (unlocked) |
| 07-config-unlocked.png | System Configuration (unlocked) |
| 08-backups-unlocked.png | Backup Repository (unlocked) |
| 09-vault-unlocked.png | Secrets Vault with masked secrets (unlocked) |
| 10-intelligence-dashboard.png | VALI Intelligence Dashboard |
| 11-intelligence-detail.png | Intelligence dashboard (alternate frame) |

## Progressive engagement (Vali mechanic)

Each deeper page required more session actions. Nav links turn green as layers unlock.
Attacker effort increases access to higher-value **decoy** surfaces — while VALI logs everything.
