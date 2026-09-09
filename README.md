# AdGuard Home Filters

Personal AdGuard Home allowlists and testing blocklists maintained in GitHub.

These lists are used with AdGuard Home and are automatically updated via GitHub Raw URLs.

---

## Repository Structure

| File | Description |
|--------|-------------|
| 🌐 `core-services.txt` | Microsoft 365, GitHub, UniFi, Cloudflare, CDNs and infrastructure services |
| 🏠 `homelab.txt` | Unraid, Docker, Jellyfin, Sonarr, Radarr, Seerr, SABnzbd, Usenet, Nextcloud, Bitwarden, AdGuard Home, NPM, Duplicati and Uptime Kuma |
| 👤 `personal.txt` | Apple, Banking, Government, PayPal, Shopping, Gaming and Popular Websites |
| 💼 `work.txt` | Employment Hero, Dayforce, Dayforce Learning and Eloomi |
| 🧪 `testing.txt` | Temporary staging area for testing new allowlist entries |
| 🚫 `testing-blocklist.txt` | Temporary staging area for testing blocklist entries |

---

## Allowlists

### Core Services

https://raw.githubusercontent.com/Jumb0King3/adguard-filters/main/allowlists/core-services.txt

### Homelab

https://raw.githubusercontent.com/Jumb0King3/adguard-filters/main/allowlists/homelab.txt

### Personal

https://raw.githubusercontent.com/Jumb0King3/adguard-filters/main/allowlists/personal.txt

### Work

https://raw.githubusercontent.com/Jumb0King3/adguard-filters/main/allowlists/work.txt

### Testing

https://raw.githubusercontent.com/Jumb0King3/adguard-filters/main/allowlists/testing.txt

---

## Blocklists

### Testing Blocklist

https://raw.githubusercontent.com/Jumb0King3/adguard-filters/main/blocklists/testing-blocklist.txt

---

## Design Philosophy

- Community-maintained blocklists provide advertising, tracking and malware protection.
- Custom allowlists provide exceptions specific to this environment.
- GitHub acts as the source of truth.
- AdGuard Home consumes all lists using Raw GitHub URLs.
- AdGuard Home caches downloaded lists locally, allowing filtering to continue during internet outages.
