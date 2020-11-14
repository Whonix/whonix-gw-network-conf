# Network Configuration for Whonix-Gateway #

Includes etc/network/interfaces.d/30_non-qubes-whonix for
Non-Qubes-Whonix-Gateway.

Sets up two network interfaces, an external one eth0 and an internal one eth1.

Provides /usr/share/whonix-gw-network-conf/network_internal_ip.txt.

DNS configuration Anonymity Linux Distribution Gateways

* Pointing /etc/resolv.conf to 127.0.0.1.
* Whether a Anonymity Linux Distribution Gateway supports system DNS for its
own traffic in the clear or anonymized mainly depends on the Gateway's
firewall.
* Routing the workstation's system DNS through the anonymizer (also known as
Transparent DNS Proxy) or not is up to the Gateway's firewall as well.
## How to install `whonix-gw-network-conf` using apt-get ##

1\. Download Whonix's Signing Key.

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

## How to Build deb Package from Source Code ##

Can be build using standard Debian package build tools such as:

```
dpkg-buildpackage -b
```

See instructions. (Replace `generic-package` with the actual name of this package `whonix-gw-network-conf`.)

* **A)** [easy](https://www.whonix.org/wiki/Dev/Build_Documentation/generic-package/easy), _OR_
* **B)** [including verifying software signatures](https://www.whonix.org/wiki/Dev/Build_Documentation/generic-package)

## Contact ##

* [Free Forum Support](https://forums.whonix.org)
* [Professional Support](https://www.whonix.org/wiki/Professional_Support)

## Donate ##

`whonix-gw-network-conf` requires [donations](https://www.whonix.org/wiki/Donate) to stay alive!
