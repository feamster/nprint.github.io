---
layout: default
title: Installation
has_children: false
parent: nPrint
grand_parent: The nPrint Project
nav_order: 1
---

# Installation

## Supported Operating Systems

* Debian Linux
* macOS

## Dependencies

* [libpcap](https://www.tcpdump.org/) - Packet sniffing
* [argp](https://www.gnu.org/software/libc/manual/html_node/Argp.html) - Argument parsing

### Install dependencies on Debian:

`sudo apt-get install libpcap-dev`

### Install dependencies on macOS

```bash
brew install argp-standalone autoconf automake libtool
```

## Install

### Building from source (latest development version)

```bash
git clone https://github.com/nprint/nprint.git
cd nprint
autoreconf -i
```

**On Debian/Linux:**
```bash
./configure
make
sudo make install
```

**On macOS:**
```bash
./configure CPPFLAGS="-I/opt/homebrew/opt/argp-standalone/include" LDFLAGS="-L/opt/homebrew/opt/argp-standalone/lib"
make
sudo make install
```

### Installing from release tarball

1. Download the latest release tar [here](https://github.com/nprint/nprint/releases/)
2. Extract the tar `tar -xvf [nprint-version.tar.gz]`
3. `cd [nprint-directory]`

**On Debian/Linux:**
```bash
./configure
make
sudo make install
```

**On macOS:**
```bash
./configure CPPFLAGS="-I/opt/homebrew/opt/argp-standalone/include" LDFLAGS="-L/opt/homebrew/opt/argp-standalone/lib"
make
sudo make install
```
