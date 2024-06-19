# stringal-utils

## nginx

### Local development with HTTPS

1. Install [mkcert](https://github.com/FiloSottile/mkcert#installation).

2. Generate a local signed certificate:

```bash
$ mkcert "localhost" "127.0.0.1" "::1" "your-LAN-ipv4"
```

3. Rename the files accordingly and move them to the `nginx` folder.

- Certificate: `.docker/nginx/ssl/localhost.pem`
- Private key: `.docker/nginx/ssl/localhost-key.pem`

4. In case you'll be accessing the web server from another
   device, [follow this](https://github.com/FiloSottile/mkcert#mobile-devices).
