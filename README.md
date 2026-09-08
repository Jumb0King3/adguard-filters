# AdGuard Home Filters

Personal AdGuard Home allowlists and testing blocklists maintained in GitHub.

These lists are used with AdGuard Home and are automatically updated via GitHub Raw URLs.

---

## Repository Structure

| File | Description |
|--------|-------------|
| 📧 `m365.txt` | Microsoft 365, Outlook, SharePoint, OneDrive, PowerShell Gallery and NuGet |
| 🐙 `github.txt` | GitHub services, releases, downloads and raw content |
| 🌐 `unifi.txt` | UniFi cloud services and account management |
| 🎬 `media-stack.txt` | Jellyfin, Sonarr, Radarr, Seerr, SABnzbd and metadata providers |
| 🐳 `docker.txt` | Docker Hub, LinuxServer.io and GitHub Container Registry |
| 💾 `unraid.txt` | Unraid services, plugins and community applications |
| ☁️ `nextcloud.txt` | Nextcloud downloads, apps and updates |
| 🔐 `bitwarden.txt` | Self-hosted Bitwarden, Duo MFA and licensing services |
| 💼 `work.txt` | Employment Hero, Dayforce and Eloomi |
| 🛒 `shopping.txt` | Bunnings, Gumtree and related shopping services |
| 🎮 `gaming.txt` | Gaming services, APIs and community resources |
| 🍎 `apple.txt` | Apple services, iCloud and Private Relay |
| 🧪 `testing.txt` | Temporary staging area for testing new allowlist entries |
| 🚫 `testing-blocklist.txt` | Temporary staging area for testing blocklist entries |

---

## Allowlists

### Microsoft 365

```text
https://raw.githubusercontent.com/Jumb0King3/adguard-filters/main/allowlists/m365.txt
```

### GitHub

```text
https://raw.githubusercontent.com/Jumb0King3/adguard-filters/main/allowlists/github.txt
```

### Infrastructure

```text
https://raw.githubusercontent.com/Jumb0King3/adguard-filters/main/allowlists/infrastructure.txt
```

### UniFi

```text
https://raw.githubusercontent.com/Jumb0King3/adguard-filters/main/allowlists/unifi.txt
```

### Media Stack

```text
https://raw.githubusercontent.com/Jumb0King3/adguard-filters/main/allowlists/media-stack.txt
```

### Unraid

```text
https://raw.githubusercontent.com/Jumb0King3/adguard-filters/main/allowlists/unraid.txt
```

### Docker

```text
https://raw.githubusercontent.com/Jumb0King3/adguard-filters/main/allowlists/docker.txt
```

### Nextcloud

```text
https://raw.githubusercontent.com/Jumb0King3/adguard-filters/main/allowlists/nextcloud.txt
```

### Bitwarden

```text
https://raw.githubusercontent.com/Jumb0King3/adguard-filters/main/allowlists/bitwarden.txt
```

### Work Services

```text
https://raw.githubusercontent.com/Jumb0King3/adguard-filters/main/allowlists/work.txt
```

### Shopping

```text
https://raw.githubusercontent.com/Jumb0King3/adguard-filters/main/allowlists/shopping.txt
```

### Gaming

```text
https://raw.githubusercontent.com/Jumb0King3/adguard-filters/main/allowlists/gaming.txt
```

### Apple

```text
https://raw.githubusercontent.com/Jumb0King3/adguard-filters/main/allowlists/apple.txt
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
