# General info about the PI

## RAM

```
cat /proc/meminfo  | grep MemTotal
```

## Auto-updates

### 1. Stop the service immediately
```
sudo systemctl stop unattended-upgrades
```

### 2. Kill any lingering apt processes
```
sudo fuser -vki /var/lib/dpkg/lock-frontend
```

### 3. Disable permanently
```
sudo dpkg-reconfigure unattended-upgrades
```

Select `<No>`
