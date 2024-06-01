# Hey! I'm Filing Here

In this lab, I successfully implemented the following TODO

## Building

```
make
```

## Running

run the executable to create cs111-base.img
```
./ext2-create 
```
dumps the filesystem information to help debug
```
dumpe2fs cs111-base.img
``` 
this will check that your filesystem is correct 
```
fsck.ext2 cs111-base.img
``` 
create a directory to mnt your filesystem 
```
mkdir mnt
```
mount your filesystem , loop lets you use a file
```
sudo mount -o loop cs111-base.img mnt
```
unmount the filesystem when you 're done
```
umount mnt
```
delete the directory used for mounting when you 're done
```
rmdir mnt
```

## Cleaning up

```
make clean
```