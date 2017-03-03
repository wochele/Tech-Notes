# Ubuntu Linode

### Initial setup

```
# Install updates
> apt-get update && apt-get upgrade

# Set hostname
> echo "<hostname>" > /etc/hostname
> hostname -F /etc/hostname
> vi /etc/hosts
  Add the line: 
  <ip address>    <hostname>

# Set timezone
> dpkg-reconfigure tzdata

