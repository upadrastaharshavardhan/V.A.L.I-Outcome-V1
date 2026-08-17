# VALI Complex Enterprise UI — Live Screenshots

Redesigned decoy portal as a **dense enterprise control plane** (sidebar + topbar + multi-panel ops UI).

## UI complexity added

- Fixed left sidebar with section groups (Operations / Platform / Data & Secrets)
- Sticky top bar with search, live status, alerts, avatar
- Metric cards, status tables, activity feeds
- Fake volume charts (bar visualization)
- Breadcrumbs, tags, unlock banners
- Split-screen login with hero metrics
- Progressive unlock indicators (green dots on unlocked modules)

## Fully unlocked path (no forbidden pages)

```
Overview → Login → Operations → Identity
  → API Gateway → Staging → Configuration
  → Backups → Secrets Vault
```

## Attack traffic mixed in

- Interactive Chrome session
- sqlmap credential probe
- gobuster / Nmap-style user agents
- Canary path `/api/v1/secrets`

## Files

| File | Screen |
|------|--------|
| 01-overview-complex.png | Overview control plane |
| 02-login-complex.png | Split-panel administrator login |
| 03-operations-complex.png | Operations dashboard |
| 04-identity-complex.png | User / identity directory |
| 05-api-gateway-complex.png | Internal API reference |
| 06-staging-complex.png | Staging control panel |
| 07-config-complex.png | System configuration + danger zone |
| 08-backups-complex.png | Backup repository |
| 09-vault-complex.png | Secrets vault |
| 10-intelligence-dashboard.png | VALI Intelligence Dashboard |

This is a **decoy**. No real credentials. Progressive engagement raises attacker cost while VALI records intelligence.
