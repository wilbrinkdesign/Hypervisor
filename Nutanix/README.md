### Create cluster

```bash
cluster -s <ip> -redundancy_factor=1 -dns_servers <dns> create
```

### SSH to AHV/CVM
```bash
ssh root@<ahv>
ssh nutanix@<cvm>
```

### Log file

```bash
cat /var/log/NTNX.serial.out.0
```

### Check all CVMs

```bash
virsh list --all
```

### Check ip CVM

```bash
virsh domifaddr <cvm>
```

### Start CVM

```bash
virsh start <cvm>
virsh autostart <cvm>
```

### Cluster health

```bash
ncc health_checks run_all
```

### Edit CVM (for example memory)

```bash
virsh edit <cvm>
```

### Set password never expires Admin user CVM

```bash
sudo chage -l admin
sudo chage -M 99999 admin
```

#### Default credentials

| Password    |
| ----------- |
| `nutanix/4u`|