# mydocker
Build a container like docker for learning cloud native.

## build
```
go build
```

## test
show usage by using stress.
### memory limit
```
./mydocker run -ti -m 100m "stress --vm-bytes 200m --vm-keep -m 1"
```

### cpu limit
```
./mydocker run -ti -cpushare 512 "stress --vm-bytes 200m --vm-keep -m 1"
```