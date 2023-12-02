# Install
### Hetzner

```Bash
cd /tmp
wget -O /tmp/talos.raw.xz https://github.com/siderolabs/talos/releases/download/v1.5.5/hcloud-amd64.raw.xz
xz -d -c /tmp/talos.raw.xz | dd of=/dev/sda && sync
shutdown -r now
```

```Bash
talosctl gen config beastvision https://88.99.82.210:6443
```

```Bash
talosctl apply-config --insecure -n 88.99.82.210 --file controlplane.yaml
```

```Bash
talosctl apply-config --insecure --nodes beast.timopollmeier.de --file controlplane.yaml
```
