# AdGuard Home Filters

Personal AdGuard Home allowlists and testing blocklists maintained in GitHub.

These lists are used with AdGuard Home and automatically updated via GitHub Raw URLs.

---

## Repository Structure

| File | Description |
|--------|-------------|
| 🌐 `core-services.txt` | Microsoft 365, GitHub, UniFi, Cloudflare, infrastructure services and common CDNs |
| 🏠 `homelab.txt` | Unraid, Docker, Jellyfin, Sonarr, Radarr, Seerr, SABnzbd, Usenet, Nextcloud, Bitwarden, AdGuard Home, NPM, Duplicati and Uptime Kuma |
| 👤 `personal.txt` | Apple, Government, Banking, Shopping, Gaming, Social Media and Popular Websites |
| 💼 `work.txt` | Employment Hero, Dayforce, Dayforce Learning, Eloomi and training platforms |
| 🧪 `testing.txt` | Temporary staging area for testing new allowlist entries |
| 🚫 `testing-blocklist.txt` | Temporary staging area for testing blocklist entries |

---

## Allowlists

### 🌐 Core Services

Microsoft 365, GitHub, UniFi, Cloudflare and Infrastructure Services.

```text
https://raw.githubusercontent.com/Jumb0King3/adguard-filters/main/allowlists/core-services.txt
```

### 🏠 Homelab

Self-hosted services running within the homelab environment.

```text
https://raw.githubusercontent.com/Jumb0King3/adguard-filters/main/allowlists/homelab.txt
```

### 👤 Personal Services

Personal, family, gaming, social media, banking and government services.

```text
https://raw.githubusercontent.com/Jumb0King3/adguard-filters/main/allowlists/personal.txt
```

### 💼 Work Services

Work, learning and employment-related services.

```text
https://raw.githubusercontent.com/Jumb0King3/adguard-filters/main/allowlists/work.txt
```

### 🧪 Testing

Temporary allowlist used for validation and troubleshooting.

```text
https://raw.githubusercontent.com/Jumb0King3/adguard-filters/main/allowlists/testing.txt
```

---

## Blocklists

### 🚫 Testing Blocklist

Temporary blocklist used to validate allowlist functionality and test new block rules.

```text
https://raw.githubusercontent.com/Jumb0King3/adguard-filters/main/blocklists/testing-blocklist.txt
```

---

## Included Services

### 🌐 Core Services

- Microsoft 365
- Outlook
- Exchange Online
- SharePoint Online
- OneDrive
- PowerShell Gallery
- NuGet
- GitHub
- UniFi
- Cloudflare
- Common CDNs
- Time Synchronisation

### 🏠 Homelab

- Unraid
- Docker Hub
- LinuxServer.io
- GitHub Container Registry
- Jellyfin
- Sonarr
- Radarr
- Seerr / Overseerr
- SABnzbd
- NewsDemon
- UsenetServer
- NZBGeek
- NZBPlanet
- NZBFinder
- AnimeTosho
- The Movie Database (TMDb)
- TheTVDB
- IMDb
- Fanart.tv
- OpenSubtitles
- MusicBrainz
- AudioDB
- OMDb
- Nextcloud
- Bitwarden
- Duo Security
- AdGuard Home
- Nginx Proxy Manager
- Let's Encrypt
- ZeroSSL
- Duplicati
- IDrive e2
- Uptime Kuma
- Crazy Domains

### 👤 Personal Services

#### Apple

- Apple
- iCloud
- Apple ID
- App Store
- Apple Private Relay

#### Australian Services

- myGov
- MyID
- ATO
- Services Australia
- Centrelink
- Commonwealth Bank
- PayPal

#### Popular Websites

- Google
- YouTube
- Reddit
- Amazon
- eBay
- Seek
- Indeed
- Gumtree
- Bunnings

#### Gaming Platforms

- Steam
- SteamCMD
- Steam Community
- Steam Workshop
- Discord
- Xbox
- PlayStation
- Epic Games
- Palworld

#### Social Media

- Twitch
- TikTok
- Facebook
- Instagram
- LinkedIn

#### Hobby Services

- Creality Cloud
- Fandom / Wikia
- Runaway Play

### 💼 Work Services

- Employment Hero
- Dayforce
- Dayforce Learning
- Eloomi
- Microsoft Stream
- Vimeo
- Brightcove

---

## Recommended Workflow

### New Allow Rule

1. Add the domain to `testing.txt`
2. Verify functionality is restored
3. Move the rule into the appropriate category file
4. Commit the change to GitHub

### New Block Rule

1. Add the domain to `testing-blocklist.txt`
2. Verify blocking behaviour
3. Move the rule to a permanent blocklist if required
4. Commit the change to GitHub

---

## Design Philosophy

- Community-maintained blocklists provide ad, tracking and malware protection.
- Custom allowlists provide exceptions specific to this environment.
- GitHub acts as the source of truth.
- AdGuard Home consumes all lists using Raw GitHub URLs.
- AdGuard Home automatically updates subscribed lists.
- AdGuard Home caches downloaded lists locally.
- DNS filtering continues working during internet outages using the most recently downloaded copy of each list.

---

## Current Environment

Services currently covered by these allowlists include:

- Microsoft 365
- AdGuard Home
- UniFi
- Unraid
- Docker
- Jellyfin
- Sonarr
- Radarr
- Seerr
- SABnzbd
- Nextcloud
- Bitwarden
- Duplicati
- Uptime Kuma
- Nginx Proxy Manager
- NewsDemon
- UsenetServer
- NZBGeek
- NZBPlanet
- NZBFinder
- AnimeTosho
- Steam
- Discord
- Commonwealth Bank
- myGov
- ATO
- Services Australia
- Centrelink
