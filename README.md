[appurl]: https://github.com/tautulli/tautulli
[fork]: https://github.com/zSeriesGuy/Tautulli

## Thanks
[Tautulli][appurl] For the original application

[zSeriesGuy][fork] For the fork

## build
To build the container
```
git clone https://github.com/ebadenes/Docker-tautulli-multi-server.git multi-tautulli
cd multi-tautulli && docker build -t ebadenes/multi-tautulli .

docker create \
  --name=tautulli \
  -v <path to data>:/config \
  -v <path to plexlogs>:/plex_logs:ro \
  -e PGID=<gid> -e PUID=<uid>  \
  -e TZ=<timezone> \
  -p 8181:8181 \
  ebadenes/multi-tautulli
```

