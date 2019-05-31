# Bitcoin Full Node, public +  tor

## Get your tor private key

No idea how to get them, but they look like this:

```rsa
-----BEGIN RSA PRIVATE KEY-----
blablabla
-----END RSA PRIVATE KEY-----
```

## Create environment file

```bash
touch .env
```

```properties
RPC_USER=myname
RPC_PASSWORD=5recgonbenuu446
BTC_DATA_DIR=./bitcoindata
```

## Audit docker-compose file

* Check both images if they are the latest versions.
* Check that the secrets file points to the correct private key file

## Run

```bash
docker-compose up -d
```
