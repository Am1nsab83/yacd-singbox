<h1 align="center">
  <img src="https://user-images.githubusercontent.com/1166872/47954055-97e6cb80-dfc0-11e8-991f-230fd40481e5.png" alt="yacd">
</h1>

> Yet Another [Clash](https://github.com/Dreamacro/clash) [Dashboard](https://github.com/Dreamacro/clash-dashboard)

## Usage

The site [http://yacd.haishan.me](http://yacd.haishan.me) ( this is not patched for singbox ) is served with HTTP not HTTPS is because many browsers block requests to HTTP resources from a HTTPS website. If you think it's not safe, you could just download the [zip of the yacd-singbox](https://github.com/Am1nsab83/yacd-singbox/releases/download/v1.1/yacd-singbox.zip), unzip and serve those static files with a web server(like Nginx).

**Docker image ( Not Patched )**

- Docker Hub [`haishanh/yacd`](https://hub.docker.com/r/haishanh/yacd)
- GitHub Container Registry [`ghcr.io/haishanh/yacd`](https://github.com/haishanh/yacd/pkgs/container/yacd)

```sh
docker run -p 1234:80 -d --name yacd --rm ghcr.io/haishanh/yacd:master

# and then open http://localhost:1234 in your browser
```

**Supported URL query params**

| Param    | Description                                                                        |
| -------- | ---------------------------------------------------------------------------------- |
| hostname | Hostname of the clash backend API (usually the host part of `external-controller`) |
| port     | Port of the clash backend API (usually the port part of `external-controller`)     |
| secret   | Clash API secret (`secret` in your config.yaml)                                    |
| theme    | UI color scheme (dark, light, auto)                                                |

## Development

```sh
# install dependencies
# you may install pnpm with `npm i -g pnpm`
pnpm i

# start the dev server
# then go to the url printed on the screen
pnpm start


# build optimized assets
# ready to deploy assets will be in the directory `public`
pnpm build
```
