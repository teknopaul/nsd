# NSD

This is a fork of [NLnetLabs/nsd](https://github.com/NLnetLabs/nsd) that enables compiling with musl-gcc on Ubuntu resulting in statically bound binary for use in LXC containers.

```
apt install git flex bison build-essential automake autoconf musl-dev musl-tools
```

## Compiling

Make sure you have the C toolchain, OpenSSL and its include files, and
libevent with its include files and flex and bison installed.
The repository does not contain ./configure and you can generate it like
this (./configure is included in release tarballs, and then you do not
have to generate it first):

```
aclocal && autoconf && autoheader
```

NSD can be compiled and installed using:

```
./configure && make && make install
```

## NSD configuration

The configuration options for NSD are described in the man pages, which are
installed (use `man nsd.conf`) and are available on the NSD
[documentation page](https://nlnetlabs.nl/documentation/nsd/).

An example configuration file is located in
[nsd.conf.sample](https://github.com/NLnetLabs/nsd/blob/master/nsd.conf.sample.in).
