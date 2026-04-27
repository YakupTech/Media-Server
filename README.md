# Self-Hosted Media Server met UGREEN NAS & Jellyfin

Een persoonlijke self-hosted media server gebouwd met een UGREEN NAS en Jellyfin.  
Het doel van dit project is om een privé media-platform te maken voor films en series, dat thuis én buitenshuis toegankelijk is via een veilige VPN-verbinding.

## Overzicht

In dit project gebruik ik een NAS als centrale thuisserver voor opslag, media-organisatie en streaming. Jellyfin draait direct op de NAS en biedt een Netflix-achtige interface voor het bekijken van films en series op telefoons, tablets, smart-tv’s en laptops.

De setup is ontworpen om te draaien zonder aparte desktopcomputer. De NAS verwerkt opslag, media streaming en containerized services.

## Hardware

- **NAS:** UGREEN NASync DXP2800
- **CPU:** Intel N100
- **Geheugen:** 8 GB DDR5, uitbreidbaar
- **Opslag:** 2-bay HDD setup
- **Netwerk:** 2.5GbE Ethernet
- **Optioneel:** NVMe SSD voor Docker/app-data

## Software Stack

| Service | Functie |
|---|---|
| Jellyfin | Media streaming server |
| Docker / Containers | Self-hosted services draaien |
| Tailscale | Veilige externe toegang via VPN |
| Sonarr | Series beheren |
| Radarr | Films beheren |
| qBittorrent / Transmission | Download client |
| Bazarr | Ondertitels beheren |
| Prowlarr | Indexers beheren |

## Functionaliteiten

- Self-hosted streaming van films en series
- Geen afhankelijkheid van commerciële streamingdiensten
- Draait direct op de NAS
- Externe toegang via Tailscale VPN
- Automatische media library scans
- Overzichtelijke mappenstructuur voor films en series
- Optionele automatisering met Sonarr en Radarr
- Persoonlijke opslag onder eigen beheer

## Mappenstructuur

```text
/media
  /movies
  /tv

/downloads
  /complete
  /incomplete

/docker
  /jellyfin
  /sonarr
  /radarr
  /qbittorrent
  /prowlarr
  /bazarr
