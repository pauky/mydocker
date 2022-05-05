# Mydocker
Build a container like docker for learning cloud native.

## Notice
restore host proc after exit from mydocker.
```
sudo mount -t proc proc /proc
```

## Build
```
go build
```

## Usage
show usage by using stress.
### memory limit
```
./mydocker run -ti -m 100m "stress --vm-bytes 200m --vm-keep -m 1"
```

### cpu limit
```
./mydocker run -ti -cpushare 512 "stress --vm-bytes 200m --vm-keep -m 1"
```

### volume
```
./mydocker run -ti -v /root/volume:/container-volume sh
```

### commit
```
./mydocker commit test-image
```
You can find file in `/root/test-image.tar`.

### detach
```
./mydocker run -d top
```

### appoint container name
```
./mydocker run -d top --name mydocker-1
```

### view log
```
./mydocker logs {your_container_name}
```