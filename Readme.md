# Deploy TBWG Blockchain POA

## 1. set password to password.txt file
```
# head -1 /dev/urandom | base64 | md5sum
```

## 2. init-genesis
```
# docker run --rm -it -v $PWD:/poa -w /poa ethereum/client-go --datadir /poa/node --nousb --password password.txt init genesis.json

```

## 3. copy static-nodes.json to node/geth
```
# cp static-nodes.json node/geth
```

## 4. deploy
```
# docker-compose up -d
# docker-compose logs -f
```