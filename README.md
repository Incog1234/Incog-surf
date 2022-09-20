# Kali-incogstealth

Incogsurf is ported to work with Kali Linux.

## How to use this repo

This repo contains the sources of both the incogsurf and pandora packages.

This repo can be compiled into a deb package to correctly install it on a Kali system.

NOTE: This may work with any debian/ubuntu system, but this has only been tested on kali-rolling amd64 system

## Usage
### Pandora
Pandora automatically overwrites the RAM when the system is shutting down. Pandora can also be ran manually:
```bash
pandora bomb
```

NOTE: This will clear the entire system cache, including active SSH tunnels or sessions.

### Incogsurf
Incogsurf will anonymize the entire system under TOR using IPTables. It will also allow you to start and stop i2p as well.

NOTE: DO NOT run this as ```service incogsurf $COMMAND```. Run this as ```incogsurf $COMMAND```

```bash
Usage:
 incogsurf {start|stop|restart|change|status}

 start - Start system-wide anonymous
          tunneling under TOR proxy through iptables
 stop - Reset original iptables settings
          and return to clear navigation
 restart - Combines "stop" and "start" options
 change - Changes identity restarting TOR 
 status - Check if IncogSurf is working properly
----[ I2P related features ]----
 starti2p - Start i2p services
 stopi2p - Stop i2p services
```

## Installation
This package comes with an installer that makes things extremely easy:

```bash
./installer.sh
```

Once the installer is complete, you will be able to use both the incogsurf and pandora modules.
