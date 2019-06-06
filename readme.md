# Bitcoin Full Node, public +  tor

## Get your tor private key

If you don't already have a tor private key, the easiest way is to just start tor from the commandline somewhere, and search the tor directories for the hostname/private_key files.

```rsa
-----BEGIN RSA PRIVATE KEY-----
blablabla
-----END RSA PRIVATE KEY-----
```

## Create environment file

First get the latest tor version using this script:
https://github.com/cmehay/docker-tor-hidden-service/blob/master/last_tor_version.sh

Create the .env file:

```bash
touch .env
```

Edit the .env file and add your preferences:

```properties
RPC_USER=myname
RPC_PASSWORD=5recgonbenuu446
BTC_DATA_DIR=./bitcoindata
TOR_VERSION=?????
TOR_PRIVATE_KEY_FILE=./private_key_blablabla
```

## Audit docker-compose file

* Check if the bitcoin image is the current latest version.
* Check that the secrets file points to your private key file

## Run

```bash
docker-compose up -d
```

Check your onion hostname:

```bash
docker exec -ti tor onions
```



## References

* Tor hidden service: https://github.com/cmehay/docker-tor-hidden-service
* Bitcoin core: https://github.com/ruimarinho/docker-bitcoin-core
