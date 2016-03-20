# livestreamer

Run [livestreamer](http://docs.livestreamer.io/) inside a Docker container.
Exposes a HTTP stream pointing to original content in port 8080.

## Example usage

```shell
docker run -p 8080:8080 blackxored/livestreamer twitch.tv/ultra best
```

## Advanced usage with config

```shell
docker run -p 8080:8080 -v ~/.livestreamerc:/root/.config/ twitch.tv/day9tv best
```

## Connecting the video player

Depending on your OS, you need to point your player to either localhost, or the IP
of your Docker linux VM. Ex: http://192.168.99.100:8080

