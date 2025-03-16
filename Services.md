# Homelab Apps and Services

| **Category**           | **Service**       | **Container Name**  | **Volume Name** | **External Domain**       | **Internal Domain**                   | **IP Address**       |
|------------------------|-------------------|---------------------|-----------------|---------------------------|---------------------------------------|----------------------|
| **Network Services**   | pfSense           | [Running on dedicated hardware] | n/a           | n/a                       | pfsense.internal.kattenhorn.tech      | 192.168.1.1          |
| **Boot Services**      | TFTP Server       | tftp-container      | tftp_data      | n/a                       | tftp.internal.kattenhorn.tech         | 192.168.1.2          |
|                        | netboot.xyz       | netboot-container   | netboot_data   | n/a                       | netboot.internal.kattenhorn.tech      | Uses TFTP IP         |
| **Dashboard**          | Glance            | glance-container    | glance_data    | glance.kattenhorn.tech    | glance.internal.kattenhorn.tech       | 192.168.1.10         |
|                        | Homarr            | homarr-container    | homarr_data    | homarr.kattenhorn.tech    | homarr.internal.kattenhorn.tech       | 192.168.1.11         |
| **Tools and Utilities**| File Browser      | filebrowser-container| fb_data       | files.kattenhorn.tech     | filebrowser.internal.kattenhorn.tech  | 192.168.1.12         |
|                        | Vaultwarden       | vaultwarden-container| vaultwarden_data| vault.kattenhorn.tech    | vaultwarden.internal.kattenhorn.tech  | 192.168.1.13         |
|                        | Hoarder           | hoarder-container   | hoarder_data   | hoarder.kattenhorn.tech   | hoarder.internal.kattenhorn.tech      | 192.168.1.14         |
|                        | Portainer         | portainer-container | portainer_data | portainer.kattenhorn.tech | portainer.internal.kattenhorn.tech    | 192.168.1.15         |
|                        | Cockpit           | cockpit-container   | cockpit_data   | cockpit.kattenhorn.tech   | cockpit.internal.kattenhorn.tech      | 192.168.1.16         |
| **Media Server**       | Jellyfin          | jellyfin-container  | jellyfin_data  | jellyfin.kattenhorn.tech  | jellyfin.internal.kattenhorn.tech     | 192.168.1.18         |
|                        | Plex              | plex-container      | plex_data      | plex.kattenhorn.tech      | plex.internal.kattenhorn.tech         | 192.168.1.19         |
|                        | Tautulli          | tautulli-container  | tautulli_data  | tautulli.kattenhorn.tech  | tautulli.internal.kattenhorn.tech     | 192.168.1.20         |
| **Media Management**   | Overseerr         | overseerr-container | overseerr_data | overseerr.kattenhorn.tech | overseerr.internal.kattenhorn.tech    | 192.168.1.21         |
|                        | Radarr            | radarr-container    | radarr_data    | radarr.kattenhorn.tech    | radarr.internal.kattenhorn.tech       | 192.168.1.22         |
|                        | Sonarr            | sonarr-container    | sonarr_data    | sonarr.kattenhorn.tech    | sonarr.internal.kattenhorn.tech       | 192.168.1.23         |
|                        | Lidarr            | lidarr-container    | lidarr_data    | lidarr.kattenhorn.tech    | lidarr.internal.kattenhorn.tech       | 192.168.1.24         |
|                        | Bazarr            | bazarr-container    | bazarr_data    | bazarr.kattenhorn.tech    | bazarr.internal.kattenhorn.tech       | 192.168.1.25         |
|                        | Prowlarr          | prowlarr-container  | prowlarr_data  | prowlarr.kattenhorn.tech  | prowlarr.internal.kattenhorn.tech     | 192.168.1.26         |
| **Download Clients**   | qBittorrent       | qbittorrent-container| qbt_data      | qbittorrent.kattenhorn.tech| qbittorrent.internal.kattenhorn.tech  | 192.168.1.27         |
|                        | NZBGet            | nzbget-container    | nzbget_data    | nzbget.kattenhorn.tech    | nzbget.internal.kattenhorn.tech       | 192.168.1.28         |
| **Files and Images**   | Nextcloud         | nextcloud-container | nextcloud_data | cloud.kattenhorn.tech     | nextcloud.internal.kattenhorn.tech    | 192.168.1.29         |
|                        | Immich            | immich-container    | immich_data    | gallery.kattenhorn.tech    | immich.internal.kattenhorn.tech       | 192.168.1.30         |
|                        | Docmost           | docmost-container   | docmost_data   | docmost.kattenhorn.tech   | docmost.internal.kattenhorn.tech      | 192.168.1.31         |
|                        | Bookstack           | bookstack-container   | bookstack_data   | bookstack.kattenhorn.tech   | bookstack.internal.kattenhorn.tech      | 192.168.1.32         |
| **Smart Home**         | Home Assistant    | hass-container      | hass_data      | hass.kattenhorn.tech      | hass.internal.kattenhorn.tech         | 192.168.1.33         |
| **DNS and Remote**     | Pi-Hole           | pihole-container    | pihole_data    | pihole.kattenhorn.tech    | pihole.internal.kattenhorn.tech       | 192.168.1.34         |
|                        | NGINX Proxy Manager| nginx-container   | nginx_data     | nginx.kattenhorn.tech     | nginx.internal.kattenhorn.tech        | 192.168.1.35         |
| **Data & Metrics**     | Grafana           | grafana-container   | grafana_data   | grafana.kattenhorn.tech   | grafana.internal.kattenhorn.tech      | 192.168.1.36         |
|                        | InfluxDB2         | influxdb-container  | influxdb_data  | influx.kattenhorn.tech    | influxdb.internal.kattenhorn.tech     | 192.168.1.37         |
| **AI** |  OpenWebUI        | openwebui-container     | openwebui_data     | openwebui.kattenhorn.tech     | openwebui.internal.kattenhorn.tech        | 192.168.1.38         |
|                       |  LiteLLM        | litellm-container     | litellm_data     | litellm.kattenhorn.tech     | litellm.internal.kattenhorn.tech        | 192.168.1.39         |
|                       | Ollama         | ollama_container | ollama_data | ollama.kattenhorn.tech | ollama.internal.kattenhorn.tech | 192.168.1.40 |
| **Collaboration** | Huly | huly_container | huly_data | huly.kattenhorn.tech | huly.internal.kattenhorn.tech | 192.168.1.41 |
|| Plane | plane_container | plane_data | plane.kattenhorn.tech | plane.internal.kattenhorn.tech | 192.168.1.42 |
|**Programming**| Gitea | gitea_container | gitea_data | git.kattenhorn.tech | git.internal.kattenhorn.tech | 192.168.1.43 |
|| SonarCube | sonar_container | sonar_data | sonar.kattenhorn.tech | sonar.internal.kattenhorn.tech | 192.168.1.44 |
| **Social Media** | Postiz | postiz_container | postiz_data | postiz.kattenhorn.tech | postiz.internal.kattenhorn.tech | 192.168.1.45 |
| **Identity** | Zitadel | zitadel_container | zitadel_data | zitadel.kattenhorn.tech | zitadel.internal.kattenhorn.tech | 192.168.1.46 |
| **Monitoring** | Checkmate | checkmate_container | checkmate_data | checkmate.kattenhorn.tech | checkmate.internal.kattenhorn.tech | 192.168.1.47|

## Notes

- **TFTP Server** and **netboot.xyz** are additional services added for network booting.
- **pfSense** acts as the main routing and firewall hardware, requiring no container.
- Continue to update the IP plan and domains according to the network needs.
- **Testing**: Ensure all services are accessible internally and externally (as permitted and secured) to verify configurations.
