# Customize for Leap-42.3 by V.Varbanovski

```bas
cd /opt/
wget ftp://ftp.freeradius.org/pub/freeradius/freeradius-server-3.0.21.tar.gz
```

- - - Need to install to compiling the freeradius-server for `OpenSUse-Leap-42.3`

```bash
zypper install libtalloc-devel gcc make 
```

- - - Compiling without SSL
```bash
cd /opt/freeradius-server-3.0.21
./configure --with-openssl=no
make 
make install
```
- - - Make executable freeradius-server for `/usr/sbin/` shell ENV
```bash
ln -s /usr/local/sbin/radiusd /usr/sbin/radiusd
```

- - - Test default config:
```bash
radiusd -X
```
- Output must be:
```xml
listen {
  	type = "auth"
  	ipaddr = *
  	port = 0
   limit {
   	max_connections = 16
   	lifetime = 0
   	idle_timeout = 30
   }
}
listen {
  	type = "acct"
  	ipaddr = *
  	port = 0
   limit {
   	max_connections = 16
   	lifetime = 0
   	idle_timeout = 30
   }
}
listen {
  	type = "auth"
  	ipv6addr = ::
  	port = 0
   limit {
   	max_connections = 16
   	lifetime = 0
   	idle_timeout = 30
   }
}
listen {
  	type = "acct"
  	ipv6addr = ::
  	port = 0
   limit {
   	max_connections = 16
   	lifetime = 0
   	idle_timeout = 30
   }
}
Listening on auth address 127.0.0.1 port 18120 bound to server inner-tunnel
Listening on auth address * port 1812 bound to server default
Listening on acct address * port 1813 bound to server default
Listening on auth address :: port 1812 bound to server default
Listening on acct address :: port 1813 bound to server default
Listening on proxy address * port 38080
Listening on proxy address :: port 53277
Ready to process requests
```
- - - Stop checking
```bash
Ctrl + C
```

