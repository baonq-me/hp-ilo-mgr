# hp-ilo-mgr

## Install HP Lights-Out Online Configuration Utility (hponcfg)

Install the required packages.

```
apt-get update
apt-get install curl
apt-get update
apt-get install curl
```

Install the required keys from HP.

```
curl https://downloads.linux.hpe.com/SDR/hpPublicKey2048.pub | apt-key add -
curl https://downloads.linux.hpe.com/SDR/hpPublicKey2048_key1.pub | apt-key add -
curl https://downloads.linux.hpe.com/SDR/hpePublicKey2048_key1.pub | apt-key add -
```

Add the HP APT-GET repository to your system.

```
add-apt-repository 'deb [arch=amd64,i386] http://downloads.linux.hpe.com/SDR/repo/mcp bionic/current non-free'
add-apt-repository 'deb [arch=amd64,i386] http://downloads.linux.hpe.com/SDR/repo/mcp bionic/10.80 non-free'
apt-get update
```

On HP server DL380 G10, Install the HP Lights-Out Online Configuration Utility using the following command.

```
apt-get install amsd
```

On HP server DL380 G9 and below, Install the HP Lights-Out Online Configuration Utility using the following command.

```
apt-get install hponcfg 
```

## Using hponcfg

To apply config

```
hponcfg -f <xml_file>
```
