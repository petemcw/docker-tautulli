# petemcw/docker-tautulli

[Tautulli](http://tautulli.com/) is a 3rd party application that you can run along side your Plex Media Server to monitor activity and track various statistics. Most importantly, these statistics include what has been watched, who watched it, when and where they watched it, and how it was watched. All statistics are presented in a nice and clean interface with many tables and graphs, which makes it easy to brag about your server to everyone else.

![](https://raw.githubusercontent.com/petemcw/docker-templates/master/petemcw/img/tautulli-banner.png)

## Usage

```bash
docker create --name=tautulli \
    -v <path to data>:/config \
    -v <path to data>:/logs:ro \
    -e PGID=<gid> \
    -e PUID=<uid> \
    -e TZ=<timezone> \
    -e 8181:8181 \
    petemcw/docker-tautulli
```

**Parameters**

* `-v /config`
* `-v /logs`
* `-e PGID` for GroupID
* `-e PUID` for UserID
* `-e TZ` for setting timezone information

## Setting up the application

Access the web-ui at <IP>:8181, for more information check out [Tautulli](http://tautulli.com/).

## Updates

* To monitor the logs of the container in real-time `docker logs -f tautulli`.

## Versions

2018.01.02 - Tautulli version 2.0.7-beta
