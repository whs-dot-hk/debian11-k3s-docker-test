# Use cgroup v1
https://docs.docker.com/config/containers/runmetrics/#changing-cgroup-version

```txt
/etc/default/grub
...
GRUB_CMDLINE_LINUX="systemd.unified_cgroup_hierarchy=0"
...
```

```sh
sudo update-grub
```

reboot

# Install docker
https://docs.docker.com/engine/install/debian/

# Run rancher
```sh
docker run -d --restart=unless-stopped \
  -p 80:80 -p 443:443 \
  --privileged \
  rancher/rancher:latest
```
