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
- Steam Dedicated Server Hosting
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

# Homelab Environment Overview

## Network Infrastructure

### UniFi Environment

#### UniFi Dream Machine Pro (UDM Pro)

Primary gateway providing:

- Internet Connectivity
- Routing
- Firewall Services
- VLAN Management
- WireGuard VPN
- UniFi Network Controller

#### UniFi Switch

**USW Pro Max 24**

Provides:

- 24 Port Switching
- 2.5GbE Connectivity
- VLAN Trunking
- Inter-VLAN Connectivity
- High-Speed Backhaul

#### Wireless

**U7 Lite**

Provides:

- Wi-Fi 7 Connectivity
- Wireless Client Access
- VLAN-Aware SSIDs
- Local Network Access

#### DNS & Filtering

- AdGuard Home
- Community-Maintained Blocklists
- GitHub-Hosted Custom Allowlists
- Local DNS Rewrites
- Automatic Filter Updates

#### Planned VLAN Layout

- Main Network
- Security Devices
- Kids Devices
- Guest / Other Devices

---

## Core Platform

### Unraid Server

Primary self-hosted platform providing:

- Container Hosting
- Data Storage
- Application Management
- Media Services
- Backup Services
- Monitoring Services

### Docker

Container platform used for all self-hosted applications.

---

## Self-Hosted Applications

### Media Stack

#### Jellyfin

Media streaming platform used for:

- Movies
- TV Shows
- Music
- Remote Family Access

Metadata Sources:

- TMDb
- TheTVDB
- IMDb
- Fanart.tv
- MusicBrainz
- AudioDB
- OMDb

#### Sonarr

TV Show automation and management.

#### Radarr

Movie automation and management.

#### Seerr

Media request and approval platform.

#### SABnzbd

Usenet download client.

---

## Usenet Services

### Providers

- NewsDemon
- UsenetServer

### Indexers

- NZBGeek
- NZBPlanet
- NZBFinder
- AnimeTosho

---

## Productivity & Collaboration

### Microsoft 365

Services in use:

- Exchange Online
- Outlook
- SharePoint Online
- OneDrive
- Microsoft Authentication
- PowerShell Management

### Nextcloud

Self-hosted file and collaboration platform.

### Bitwarden

Self-hosted password management platform.

### Employment Services

- Employment Hero
- Dayforce
- Dayforce Learning
- Eloomi

---

## Infrastructure Services

### Nginx Proxy Manager (NPM)

Reverse proxy and SSL management.

Certificate Providers:

- Let's Encrypt
- ZeroSSL

### Uptime Kuma

Service and availability monitoring.

### Duplicati

Backup management platform.

Backup Destination:

- IDrive e2

### GitHub

Source of truth for:

- AdGuard Allowlists
- Configuration Documentation
- Change Tracking
- Version Control

---

## Domain & DNS Providers

### Crazy Domains

- Domain Registration
- DNS Management

### Cloudflare

- DNS Services
- CDN Services
- Security Services

---

## Current Environment

### Network

- UniFi Dream Machine Pro (UDM Pro)
- USW Pro Max 24
- U7 Lite
- AdGuard Home

### Infrastructure

- Unraid
- Docker
- Nginx Proxy Manager
- Uptime Kuma

### Media

- Jellyfin
- Sonarr
- Radarr
- Seerr
- SABnzbd

### Usenet

- NewsDemon
- UsenetServer

### Indexers

- NZBGeek
- NZBPlanet
- NZBFinder
- AnimeTosho

### Productivity

- Microsoft 365
- Nextcloud
- Bitwarden

### Backup

- Duplicati
- IDrive e2

### Domain & DNS

- Crazy Domains
- Cloudflare

### Source Control

- GitHub

---

## Design Principles

- Community-maintained blocklists
