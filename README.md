# media-stack
Home media stack


- docker network create mediastack
- cp .env.example .env
- update .env configuration with directory structure, or update volume with overwritten `docker-compose.override.yml`


- Login to Jackett, Jellyfin, Prowlarr, Radarr, Sonarr using `http://localhost:[ORIGINAL_PORT]`, update their base URL to subfolder accordinglly. Save and restart containers.


Then you should be able to access services as:
- Jellyseerr: http://localhost:8080/
- Jellyfin: http://localhost:8080/jellyfin
- Jackett: http://localhost:8080/jackett
- Prowlarr: http://localhost:8080/prowlarr
- Radarr: http://localhost:8080/radarr
- Sonarr: http://localhost:8080/sonarr


You can setup a domain using nginx reverse proxy to forward requests to http://localhost:8080 + SSL certificates.


## Notes
- Download clients is not included, you can install it separately, e.g. qBittorrent
