# livestreamer

[![](https://images.microbadger.com/badges/image/blackxored/livestreamer.svg)](http://microbadger.com/#/images/blackxored/livestreamer)

Run [livestreamer](http://docs.livestreamer.io/) inside a Docker container.
Exposes a HTTP stream pointing to original content in port 8080.

## Usage

### Simple usage


```shell
docker run --rm --net=host blackxored/livestreamer twitch.tv/ultra best
```

### Explicit port mapping

Container exposes streaming server at port 8080.

```shell
docker run --rm -p 8080:8080 blackxored/livestreamer twitch.tv/ultra
```

### Advanced usage with config

For logging in and setting extra configuration options, you may mount
a file as a directory inside the container.

```shell
docker run --rm -p 8080:8080 -v ~/.livestreamerrc:/root/.livestreamerrc blackxored/livestreamer twitch.tv/ultra best
```

You can easily leverage this by creating a shell alias:

```shell
alias livestreamer="docker run -rm -p 8080:8080 -v ~/.livestreamerrc:/root/.livestreamerrc blackxored/livestreamer"
```

And then use it like:

```
livestreamer twitch.tv/ultra best
```

## Connecting the video player

Depending on your OS, you need to point your player to either localhost, or the IP
of your Docker Linux VM. Ex: http://192.168.99.100:8080


## License

For license information on the software included in this image, see
[Livestreamer LICENSE](https://github.com/chrippa/livestreamer/blob/develop/LICENSE).

## Contributing

1. Fork it ( https://github.com/blackxored/docker-livestreamer/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request

