# Homelab Apps and Services

| **Category**           | **Service**       | **Container Name**  | **Volume Name** | **External Domain**       | **Internal Domain**                   | **IP Address** |  **Website URL** |
|------------------------|-------------------|---------------------|-----------------|---------------------------|---------------------------------------|----------------|------------------|
| **Boot Services**      | TFTP Server       | tftp-container      | tftp_data       | n/a                       | tftp.khn.family                       | 192.168.1.2    |                  |
|                        | netboot.xyz       | netboot-container   | netboot_data    | n/a                       | netboot.khn.family                    | Uses TFTP IP   | [netboot.xyz](https://netboot.xyz) |
| **Dashboard**          | Glance            | glance-container    | glance_data     | glance.khn.family         | glance.khn.family                     | 192.168.1.11   | [glance](https://github.com/glanceapp/glance) |
|                        | Homarr            | homarr-container    | homarr_data     | homarr.khn.family         | homarr.khn.family                     | 192.168.1.11   | [homarr.dev](https://homarr.dev/) |
| **Tools and Utilities**| File Browser      | filebrowser-container| fb_data        | files.khn.family          | filebrowser.khn.family                | 192.168.1.11   | [filebrowser.org](https://filebrowser.org) |
|                        | Vaultwarden       | vaultwarden-container| vaultwarden_data| vault.khn.family         | vaultwarden.khn.family                | 192.168.1.11   | [bitwarden.com](https://bitwarden.com) |
|                        | Hoarder           | hoarder-container   | hoarder_data   | hoarder.khn.family         | hoarder.khn.family                    | 192.168.1.11   | [hoarder.app](https://hoarder.app) |
|                        | Portainer         | portainer-container | portainer_data | portainer.khn.family       | portainer.khn.family                  | 192.168.1.11   | [portainer.io](https://www.portainer.io) |
|                        | Cockpit           | cockpit-container   | cockpit_data   | cockpit.khn.family         | cockpit.khn.family                    | 192.168.1.11   | [cockpit-project.org](https://cockpit-project.org) |
| **Media Server**       | Jellyfin          | jellyfin-container  | jellyfin_data  | jellyfin.khn.family        | jellyfin.khn.family                   | 192.168.1.11   | [jellyfin.org](https://jellyfin.org) |
|                        | Plex              | plex-container      | plex_data      | plex.khn.family            | plex.khn.family                       | 192.168.1.11   | [plex.tv](https://www.plex.tv) |
|                        | Tautulli          | tautulli-container  | tautulli_data  | tautulli.khn.family        | tautulli.khn.family                   | 192.168.1.11   | [tautulli.com](https://tautulli.com) |
| **Media Management**   | Overseerr         | overseerr-container | overseerr_data | guide.khn.family           | guide.khn.family                      | 192.168.1.11   | [overseerr.dev](https://overseerr.dev) |
|                        | Radarr            | radarr-container    | radarr_data    | radarr.khn.family          | radarr.khn.family                     | 192.168.1.11   | [radarr.video](https://radarr.video) |
|                        | Sonarr            | sonarr-container    | sonarr_data    | sonarr.khn.family          | sonarr.khn.family                     | 192.168.1.11   | [sonarr.tv](https://sonarr.tv) |
|                        | Lidarr            | lidarr-container    | lidarr_data    | lidarr.khn.family          | lidarr.khn.family                     | 192.168.1.11   | [lidarr.audio](https://lidarr.audio) |
|                        | Bazarr            | bazarr-container    | bazarr_data    | bazarr.khn.family          | bazarr.khn.family                     | 192.168.1.11   | [bazarr.media](https://www.bazarr.media) |
|                        | Prowlarr          | prowlarr-container  | prowlarr_data  | prowlarr.khn.family        | prowlarr.khn.family                   | 192.168.1.11   | [prowlarr.com](https://prowlarr.com) |
| **Download Clients**   | qBittorrent       | qbittorrent-container| qbt_data      | qbittorrent.khn.family     | qbittorrent.khn.family                | 192.168.1.11   | [qbittorrent.org](https://www.qbittorrent.org) |
|                        | NZBGet            | nzbget-container    | nzbget_data    | nzbget.khn.family          | nzbget.khn.family                     | 192.168.1.11   | [nzbget.net](https://nzbget.net) |
| **Files and Images**   | Nextcloud         | nextcloud-container | nextcloud_data | cloud.khn.family           | cloud.khn.family                      | 192.168.1.11   | [nextcloud.com](https://nextcloud.com) |
|                        | Immich            | immich-container    | immich_data    | photos.khn.family          | photos.khn.family                     | 192.168.1.11   | [immich.app](https://immich.app) |
|                        | Docmost           | docmost-container   | docmost_data   | docmost.khn.family         | docmost.khn.family                    | 192.168.1.11   | [docmost.com](https://docmost.com) |
|                        | Bookstack         | bookstack-container | bookstack_data | bookstack.khn.family       | bookstack.khn.family                  | 192.168.1.11   | [bookstackapp.com](https://www.bookstackapp.com) |
| **Smart Home**         | Home Assistant    | hass-container      | hass_data      | hass.khn.family            | hass.khn.family                       | 192.168.1.11   | [home-assistant.io](https://www.home-assistant.io) |
| **DNS and Remote**     | Pi-Hole           | pihole-container    | pihole_data    | pihole.khn.family          | pihole.khn.family                     | 192.168.1.2    | [pi-hole.net](https://pi-hole.net) |
|                        | Traefik           | traefik             | traefik_data   | traefik.khn.family         | traefik.khn.family                    | 192.168.1.11   | [traefik.io](https://traefik.io) |
| **Data & Metrics**     | Grafana           | grafana-container   | grafana_data   | grafana.khn.family         | grafana.khn.family                    | 192.168.1.11   | [grafana.com](https://grafana.com) |
|                        | InfluxDB2         | influxdb-container  | influxdb_data  | influx.khn.family          | influxdb.khn.family                   | 192.168.1.11   | [influxdata.com](https://www.influxdata.com) |
| **AI**                 | OpenWebUI         | openwebui-container | openwebui_data | ai.khn.family              | ai.khn.family                         | 192.168.1.12   | [openwebui.com](https://openwebui.com) |
|                        | LiteLLM           | litellm-container   | litellm_data   | litellm.khn.family         | litellm.khn.family                    | 192.168.1.12   | [litellm.ai](https://litellm.ai) |
|                        | Ollama            | ollama_container    | ollama_data    | ollama.khn.family          | ollama.khn.family                     | 192.168.1.12   | [ollama.ai](https://ollama.ai) |
| **Collaboration**      | Huly              | huly_container      | huly_data      | huly.khn.family            | huly.khn.family                       | 192.168.1.11   | [huly.io](https://huly.io) |
|                        | Plane             | plane_container     | plane_data     | plane.khn.family           | plane.khn.family                      | 192.168.1.11   | [plane.so](https://plane.so) |
| **Programming**        | Gitea             | gitea_container     | gitea_data     | git.khn.family             | git.khn.family                        | 192.168.1.11   | [gitea.io](https://gitea.io) |
|                        | SonarCube         | sonar_container     | sonar_data     | sonar.khn.family           | sonar.khn.family                      | 192.168.1.11   | [sonarqube](https://www.sonarsource.com/products/sonarqube) |
| **Social Media**       | Postiz            | postiz_container    | postiz_data    | postiz.khn.family          | postiz.khn.family                     | 192.168.1.11   | [postiz.com](https://postiz.com) |
| **Identity**           | Zitadel           | zitadel_container   | zitadel_data   | zitadel.khn.family         | zitadel.khn.family                    | 192.168.1.11   | [zitadel.com](https://zitadel.com) |
| **Monitoring**         | Checkmate         | checkmate_container | checkmate_data | checkmate.khn.family       | checkmate.khn.family                  | 192.168.1.11   | [checkmate.so](https://checkmate.so) |

## Notes

- **TFTP Server** and **netboot.xyz** are additional services added for network booting.
- **pfSense** acts as the main routing and firewall hardware, requiring no container.
- **Testing**: Ensure all services are accessible internally and externally (as permitted and secured) to verify configurations.
