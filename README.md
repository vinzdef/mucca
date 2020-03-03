# mucca
![a mucca does what she wants because a mucca is free](./docs/mucca.jpg)

## AIO solution to download and manage your media files!

Mucca is a set of software commonly used for to download, manage and consume media files, namedly:

+ [Sonarr](https://github.com/Sonarr/Sonarr) — TV Series
+ [Radarr](https://github.com/Radarr/Radarr) — Movies
+ [Bazaar](https://github.com/morpheus65535/bazarr) — Subtitles
+ [Lidarr](https://github.com/lidarr/Lidarr) — Music
+ [Plex](https://www.plex.tv/) — Library & Streaming
+ [Deluge](https://github.com/deluge-torrent/deluge) — BitTorrent service
+ [Jacket](https://github.com/Jackett/Jackett) — Torrent trackers aggregator

### Installation

Just download this repo, then: `docker-compose up -d`

You will find all the services on your `localhost` at their default ports:
+ **Sonarr**: `:8989`
+ **Radarr**: `:7878`
+ **Bazaar**: `:6767`
+ **Lidarr**: `:8686`
+ **Plex**:   `:32400`
+ **Deluge**: `:8112`
+ **Jacket**: `:9117`


This will start all the services in the background.

Now you need:
+ Pick a password for deluge, or disable it altogether along with any other option you may want to touch.
+ Tell library agents (Sonarr, Radarr, Lidarr) where to find your torrent client (Deluge), this can be done in their respective settings.
+ Add your chosen trackers in Jackett, then go to the libraries (as above) and use jackett's aggregated endpoint to search 'em all.
+ Configure Plex on it's page.
+ ...
+ Profit!
