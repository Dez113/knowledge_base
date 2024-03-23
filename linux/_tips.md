# Tips, commands, etc.

### Clean memory cache cmd 
There is an opinion this trick is from Cargo cult administrators... It will drops the cache, but than kernel needs to load all data from the disk.
- 1 - means clear PageCache only
- 2 - clear dentries and inodes
- 3 - clear all previous
```
sudo sh -c "sync; echo 1 > /proc/sys/vm/drop_caches"
```
