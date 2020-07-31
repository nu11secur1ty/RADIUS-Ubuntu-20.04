# Download source

```bas
cd /opt/
wget ftp://ftp.freeradius.org/pub/freeradius/freeradius-server-3.0.21.tar.gz
```

- - - Need to install to compilig the freeradius-server for `OpenSUse-Leap-42.3`

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

