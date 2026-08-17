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

01-HOME
<img width="1440" height="900" alt="01-home" src="https://github.com/user-attachments/assets/ea5ebd6e-ef1d-45a5-9963-cfd71027e483" />
02-LOGIN 
<img width="1440" height="900" alt="02-login" src="https://github.com/user-attachments/assets/b429e21a-94b6-446e-b3b8-3b13f925462d" />
03-dashboard-decoy
<img width="1440" height="900" alt="03-dashboard-decoy" src="https://github.com/user-attachments/assets/86c6e9a6-d021-481d-a5d8-92fc3702b0aa" />
04-users
<img width="1440" height="900" alt="04-users" src="https://github.com/user-attachments/assets/f8b2afb8-bf09-41a3-ad73-8d5d06784806" />
05-api-docs
<img width="1440" height="900" alt="05-api-docs" src="https://github.com/user-attachments/assets/dd48cd02-bff4-4c62-ab14-da8ead027521" />
06-staging
<img width="1440" height="900" alt="06-staging" src="https://github.com/user-attachments/assets/546c1d60-faaf-4c35-8b72-74d5b1e9f3fb" />
07-config
<img width="1440" height="900" alt="07-config" src="https://github.com/user-attachments/assets/af9ad5c5-24c3-4f3a-a678-cfbacc4bfec9" />
08-backups
<img width="1440" height="900" alt="08-backups" src="https://github.com/user-attachments/assets/545cfe4c-59dd-4dc2-96c6-2c0307f14647" />
09-vault
<img width="1440" height="900" alt="09-vault" src="https://github.com/user-attachments/assets/d1094012-6b96-4b29-bdb2-0ac17ce80dfb" />
10-intelligence-dashboard
<img width="1440" height="1100" alt="10-intelligence-dashboard" src="https://github.com/user-attachments/assets/4d7da4c0-139c-4e36-a65c-019262273ba2" />

## How the flow works

1. Attacker lands on **home** (looks like a real internal portal)
2. Tries **login** → failed attempts logged as credential_access
3. Explores **dashboard / users** → recon + discovery
4. Progressive unlocks reveal **API docs → staging → config → backups → vault**
5. Touching vault / secrets paths triggers **canaries**
6. Logger scores risk, tags kill-chain, profiles attacker
7. **Intelligence Dashboard** shows sessions, campaigns, canaries, blocklist

Attackers spend. Defenders learn.
