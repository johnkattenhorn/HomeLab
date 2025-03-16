# Homelab Hardware and Configuration

## Hardware Specs

- Insert Specs from Spreasheet here once it's built

## Software Specs

- Proxmox OS

### Proxmox Configuration

### ZFS Configuration for Proxmox

#### SSD Configuration

- **Purpose**: Fast storage for virtual machines and containers, databases, and frequently accessed files.
- **ZFS Pool Name**: `ssd_pool`
- **RAID Level**: RAID-Z1 (similar to RAID 5) - This allows the loss of one disk without data loss while providing a good balance between storage capacity, performance, and redundancy.

**Configuration**:

```plaintext
zpool create ssd_pool raidz1 /dev/sda /dev/sdb /dev/sdc /dev/sdd
```

- **Volume Name**: `ssd_storage`
- **Container and VM Datastore**: Use this SSD pool mainly for the VM and container storage to take advantage of higher IOPS.

#### HDD Configuration

- **Purpose**: Large storage capacity for media files, backups, and less frequently accessed data.
- **ZFS Pool Name**: `hdd_pool`
- **RAID Level**: RAID-Z (similar to RAID 5 but optimized for larger disks) - This provides redundancy through parity and can tolerate the failure of one disk.

**Configuration**:

```plaintext
zpool create hdd_pool raidz /dev/sde /dev/sdf /dev/sdg
```

- **Volume Name**: `hdd_storage`
- **Storage Usage**: Use this pool to store media files (movies, music), less time-sensitive backups, and archival data, taking advantage of the large capacity.

### Naming and Allocation

- **Storage Naming**: Keep names intuitive like `ssd_pool`, `ssd_storage`, `hdd_pool`, and `hdd_storage`.
- **Data Allocation**:
  - Place VMs, container images, and any applications requiring fast read/write (like databases and frequently accessed apps) on `ssd_storage`.
  - Store larger, less frequently accessed files such as media libraries and archives on `hdd_storage`.
