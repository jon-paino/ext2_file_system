# Hey! I'm Filing Here

The lab involves constructing a makeshift ext2 file system by setting up a disk image to simulate storage, creating necessary data structures like inodes and directory entries, and implementing functions for file creation, deletion, and reading. You initialized the disk image, allocated space for superblock, group descriptor, block bitmap, inode bitmap, inode table, and data blocks, then implemented file operations by manipulating these structures to mimic ext2 behavior. This included writing code to handle block allocation, directory management, and file system consistency.

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