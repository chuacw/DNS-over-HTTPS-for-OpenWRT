# DNS-over-HTTPS-for-OpenWRT
DNS over HTTPS for OpenWRT/LEDE routers

Provides the DNS over HTTPS init.d script and configuration for the dnscrypt-proxy app from https://github.com/jedisct1/dnscrypt-proxy/

* Place the dnscrypt-proxy in /etc/init.d and chmod a+x
* Place the dnscrypt-proxy.toml in /etc/config
* Download the app from https://github.com/jedisct1/dnscrypt-proxy/ and place the executable in /usr/sbin/
* /etc/init.d/dnscrypt-proxy enable
* /etc/init.d/dnscrypt-proxy start

If you use dnsmasq, edit /etc/dnsmasq.conf so that the listening port is not conflicting with dnscrypt-proxy's. Set port=5053 for example, in /etc/dnsmasq.conf and set dhcp-option=3,x.x.x.x and dhcp-option=6,x.x.x.x where x.x.x.x is your router IP so that your router's dnscrypt-proxy is used to resolve the DNS.

