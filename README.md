# Dante

## Running

```
$ PROXY_USER=username
$ PROXY_PASS=password
$ docker run -d --rm --name dante -p 1080:1080 --env PROXY_USER=$PROXY_USER --env PROXY_PASS=$PROXY_PASS alexvv/dante
```

## Verify
```
$ curl -x socks5h://$PROXY_USER:$PROXY_PASS@127.0.0.1:1080 https://google.com
```