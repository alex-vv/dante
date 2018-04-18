# Dante

## Running

```
$ DANTE_USER=username
$ DANTE_PASS=password
$ docker run -d --rm --name dante -p 1080:1080 alexvv/dante
$ docker exec dante bash -c "adduser -D $DANTE_USER;echo $DANTE_USER:$DANTE_PASS | chpasswd"
```

## Verify
```
$ curl -x socks5h://$DANTE_USER:$DANTE_PASS@127.0.0.1:1080 https://google.com
```