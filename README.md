# mediumz-demo

Medium.com reversed proxy demo.

## Usage

### Docker

Using [OrbStack](https://orbstack.dev/) to automatically configure HTTPS based on the container name.

```bash
docker build -t mediumz-demo .
docker run \
    --name mediumz-demo \
    -e DOMAIN=mediumz-demo.orb.local \
    mediumz-demo
```

Visit: `https://mediumz-demo.orb.local`

### Using native nginx installed on your system

Required module [http_sub_module](https://nginx.org/en/docs/http/ngx_http_sub_module.html)

Copy contents of [templates/default.conf.template](templates/default.conf.template) file and replace `${DOMAIN}` with your domain.
