# Deploy TBWG Blockchain POA

## 1. set password to password.txt file
```
# head -1 /dev/urandom | base64 | md5sum
```

## 2. init-genesis
```
# ./init-genesis.sh
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