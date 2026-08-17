# VALI Live Run Screenshots

Captured from a real local run of **VALI v10** with simulated attacker traffic.

## Traffic simulated (realistic tooling signatures)

- Nmap Scripting Engine user-agent (scanner)
- sqlmap user-agent (injection probing)
- gobuster user-agent (directory busting)
- Chrome browser (interactive)

## Results from this run

- Multiple sessions created
- Risk scores up to **100** (targeted)
- Profiles: automated, interactive, targeted
- Tools detected: browser, dirbuster, scanner, script, sqlmap
- Kill-chain tags: recon, credential_access, discovery, collection, high_value, progress
- Canary hits recorded

## Screenshot index

| File | What it shows |
|------|----------------|
| 01-home.png | Decoy home — NexusOps Internal Admin Portal |
| 02-login.png | Login surface (credential harvesting stage) |
| 03-dashboard-decoy.png | Fake internal dashboard |
| 04-users.png | User management decoy table |
| 05-api-docs.png | API docs layer (progressive unlock) |
| 06-staging.png | Staging environment layer |
| 07-config.png | Config panel layer |
| 08-backups.png | Backup files layer |
| 09-vault.png | Secrets vault (high-value / canary) |
| 10-intelligence-dashboard.png | VALI Intelligence Dashboard (sessions, risk, kill-chain) |

## How the flow works

1. Attacker lands on **home** (looks like a real internal portal)
2. Tries **login** → failed attempts logged as credential_access
3. Explores **dashboard / users** → recon + discovery
4. Progressive unlocks reveal **API docs → staging → config → backups → vault**
5. Touching vault / secrets paths triggers **canaries**
6. Logger scores risk, tags kill-chain, profiles attacker
7. **Intelligence Dashboard** shows sessions, campaigns, canaries, blocklist

Attackers spend. Defenders learn.
