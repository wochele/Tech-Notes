# Proxy

### Setting up a proxy

```
> npm config set proxy http://proxy_host:port
> npm config set https-proxy http://proxy.company.com:8080

// Setting up proxy with AD credentials, URL encode the \
> npm config set proxy http://DOMAIN%5CUserName:Password@EBCSWG.bmogc.net:8080
> npm config set https-proxy http://DOMAIN%5CUserName:Password@EBCSWG.bmogc.net:8080

```

### Removing a proxy setting

```
> npm config rm proxy
> npm config rm https-proxy
```

### Get current npm settings

```
> npm config get
```

- Settings are kept in `.npmrc` in c:\users\username
