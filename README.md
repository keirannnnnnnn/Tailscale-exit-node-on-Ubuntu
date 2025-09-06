# Tailscale-exit-node-on-Ubuntu
Allow Tailscale Exit Node from Ubuntu

Once tailscale is installed, run the following in terminal to allow tailscale to share the local network connection

```
echo 'net.ipv4.ip_forward = 1' | sudo tee -a /etc/sysctl.d/99-tailscale.conf
echo 'net.ipv6.conf.all.forwarding = 1' | sudo tee -a /etc/sysctl.d/99-tailscale.conf
sudo sysctl -p /etc/sysctl.d/99-tailscale.conf
```
