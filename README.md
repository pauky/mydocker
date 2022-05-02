# mydocker
Build a container like docker for learning cloud native.

## notice
restore host proc after exit from mydocker.
```
sudo mount -t proc proc /proc
```

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