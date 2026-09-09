# AdGuard Home Filters

Personal AdGuard Home allowlists and testing blocklists maintained in GitHub.

These lists are used with AdGuard Home and are automatically updated via GitHub Raw URLs.

---

## Repository Structure

| File | Description |
|--------|-------------|
| 🌐 `core-services.txt` | Microsoft 365, GitHub, UniFi, Cloudflare, CDNs and infrastructure services |
| 🏠 `homelab.txt` | Unraid, Docker, Jellyfin, Sonarr, Radarr, Seerr, SABnzbd, Nextcloud and Bitwarden |
| 👤 `personal.txt` | Apple, Banking, Government, PayPal, Shopping, Gaming and Popular Websites |
| 💼 `work.txt` | Employment Hero, Dayforce, Dayforce Learning and Eloomi |
| 🧪 `testing.txt` | Temporary staging area for testing new allowlist entries |
| 🚫 `testing-blocklist.txt` | Temporary staging area for testing blocklist entries |

---

## Allowlists

### Core Services

```text
https://raw.githubusercontent.com/Jumb0King3/adguard-filters/main/allowlists/core-services.txt
```

### Homelab

```text
https://raw.githubusercontent.com/Jumb0King3/adguard-filters/main/allowlists/homelab.txt
```

### Personal Services

```text
https://raw.githubusercontent.com/Jumb0King3/adguard-filters/main/allowlists/personal.txt
```

### Work Services

```text
https://raw.githubusercontent.com/Jumb0King3/adguard-filters/main/allowlists/work.txt
```

### Testing

```text
https://raw.githubusercontent.com/Jumb0King3/adguard-filters/main/allowlists/testing.txt
```

---

## Blocklists

### Testing Blocklist

```text
https://raw.githubusercontent.com/Jumb0King3/adguard-filters/main/blocklists/testing-blocklist.txt
```

---

## What's Included

### 🌐 Core Services

- Microsoft 365
- Outlook
- SharePoint
- OneDrive
- GitHub
- UniFi
- Cloudflare
- Common CDNs
- Time Synchronisation

### 🏠 Homelab

- Unraid
- Docker
- LinuxServer.io
- Jellyfin
- Sonarr
- Radarr
- Seerr
- SABnzbd
- Nextcloud
- Self-hosted Bitwarden

### 👤 Personal Services

- Apple & iCloud
- Apple Private Relay
- Commonwealth Bank
- myGov
- ATO
- Services Australia
- Centrelink
- PayPal
- Google
- YouTube
- Reddit
- Amazon
- eBay
- Seek
- Indeed
- Gumtree
- Bunnings
- Palworld
- Creality
- Fandom

### 💼 Work Services

- Employment Hero
- Dayforce
- Dayforce Learning
- Eloomi

---

## Recommended Workflow

### New Allow Rule

1. Add the domain to `testing.txt`
2. Verify the issue is resolved
3. Move the rule to the appropriate category file
4. Commit the change to GitHub

### New Block Rule

1. Add the domain to `testing-blocklist.txt`
2. Verify the domain is blocked as expected
3. Move the rule to a permanent blocklist if required
4. Commit the change to GitHub

---

## Design Philosophy

- Community-maintained blocklists provide advertising, tracking and malware protection.
- Custom allowlists provide exceptions specific to this environment.
- GitHub acts as the source of truth.
- AdGuard Home consumes all lists using Raw GitHub URLs.
- AdGuard Home caches downloaded lists locally, allowing filtering to continue during internet outages.
