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

1\. Download the APT Signing Key.

```
wget https://www.whonix.org/keys/derivative.asc
```

Users can [check the Signing Key](https://www.whonix.org/wiki/Signing_Key) for better security.

2\. Add the APT Signing Key.

```
sudo cp ~/derivative.asc /usr/share/keyrings/derivative.asc
```

3\. Add the derivative repository.

```
echo "deb [signed-by=/usr/share/keyrings/derivative.asc] https://deb.whonix.org trixie main contrib non-free" | sudo tee /etc/apt/sources.list.d/derivative.list
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

See instructions.

NOTE: Replace `generic-package` with the actual name of this package `whonix-gw-network-conf`.

* **A)** [easy](https://www.whonix.org/wiki/Dev/Build_Documentation/generic-package/easy), _OR_
* **B)** [including verifying software signatures](https://www.whonix.org/wiki/Dev/Build_Documentation/generic-package)

## Contact ##

* [Free Forum Support](https://forums.whonix.org)
* [Premium Support](https://www.whonix.org/wiki/Premium_Support)

## Donate ##

`whonix-gw-network-conf` requires [donations](https://www.whonix.org/wiki/Donate) to stay alive!
