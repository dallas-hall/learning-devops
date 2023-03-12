# Network Basics

I basically knew most of this already from the excellent [CKAD](https://github.com/dallas-hall/learning-containers-and-orchestration/tree/main/kubernetes/02.applications-developer), [CKA](https://github.com/dallas-hall/learning-containers-and-orchestration/tree/main/kubernetes/03.administrator), and [CKS](https://github.com/dallas-hall/learning-containers-and-orchestration/tree/main/kubernetes/04.security) courses that I did. So the only thing documented here is course specific or something I didn't know.

## Networking

```bash
# View the host interfaces
ip link

# View the host IP addresses
ip addr

# Add an IP address to an interface
ip addr add $IP_ADDRESS dev $INTERFACE
```

![](images/networking01.png)

* A router needs to have an IP address assigned to it from each network it is connecting.

![](images/networking02.png)

```bash
# Add a gateway route
ip route add $TARGET_CIDR via $ROUTER_IP
```

* The gateway needs to be configured on all systems.

![](images/networking03.png)

* The default gateway also needs to be configured on all systems.

![](images/networking04.png)

* The above networking routing can be simplified to the picture below.
*`default` and `0.0.0.0` entries in the Destination field means the same thing, which is route any unknown IP address to the default gateway. So the first 2 lines in the above picture mean the same thing.
* The `0.0.0.0` entry in the Gateway means that you don't need a gateway. This is to handle internal private network between devices within the same network.

![](images/networking05.png)

* By default in Linux packets are not forwarded between interfaces. This is a security feature.

![](images/networking06.png)

* You can check packet forwarding between interfaces at `/proc/sys/net/ipv4/ip_forward` and you can permanently toggle it in `/etc/sysctl.conf` via the `net.ipv4.ip_forward` entry.

![](images/networking07.png)

## DNS

* Entries within `/etc/hosts` are considered truthful and not verified. This can be use for normal and malicious purposes.

![](images/dns01.png)

* The DNS Name Server is configured in `/etc/resolv.conf` using `nameserver $IP_ADDRESS`

![](images/dns02.png)

* The DNS resolution order can be configured in `/etc/nsswitch.conf` where `files` is for local DNS resolution and `dns` is for a DNS Nameserver resolution.
* In the picture below the default is displayed, which is local DNS resolution and then DNS Name Server resolution.

![](images/dns03.png)

* You will likely want to add a `nameserver $IP_ADDRESS` entry into `/etc/resolv.conf` for an Internet DNS Name Server like Google or Cloud Flare so you can resolve internet resources.

![](images/dns04.png)

* The result of DNS resolution is typically cached temporarily so the same lookup isn't made multipe times. This is typically a few seconds to a few minutes.

![](images/dns05.png)

* Add `search $DOMAIN` into `/etc/resolv.conf` to tell the DNS Name Server to search that domain for hosts without using the FDQN.

![](images/dns06.png)
