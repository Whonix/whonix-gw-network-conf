# Network Configuration for Whonix-Gateway #

Includes etc/network/interfaces.d/30_non-qubes-whonix for
Non-Qubes-Whonix-Gateway.

Sets up two network interfaces, an external one eth0 and an internal one eth1.

Provides /usr/share/whonix-gw-network-conf/network_internal_ip.txt.
## How to install `whonix-gw-network-conf` using apt-get ##

1\. Download [Whonix's Signing Key]().

```
wget https://www.whonix.org/patrick.asc
```

Users can [check Whonix Signing Key](https://www.whonix.org/wiki/Whonix_Signing_Key) for better security.

2\. Add Whonix's signing key.

```
sudo apt-key --keyring /etc/apt/trusted.gpg.d/whonix.gpg add ~/patrick.asc
```

3\. Add Whonix's APT repository.

```
echo "deb https://deb.whonix.org buster main contrib non-free" | sudo tee /etc/apt/sources.list.d/whonix.list
```

4\. Update your package lists.

```
sudo apt-get update
```

5\. Install `whonix-gw-network-conf`.

```
sudo apt-get install whonix-gw-network-conf
```

## How to Build deb Package ##

Replace `apparmor-profile-torbrowser` with the actual name of this package with `whonix-gw-network-conf` and see [instructions](https://www.whonix.org/wiki/Dev/Build_Documentation/apparmor-profile-torbrowser).

## Contact ##

* [Free Forum Support](https://forums.whonix.org)
* [Professional Support](https://www.whonix.org/wiki/Professional_Support)

## Donate ##

`whonix-gw-network-conf` requires [donations](https://www.whonix.org/wiki/Donate) to stay alive!
