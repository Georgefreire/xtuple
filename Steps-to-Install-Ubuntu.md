xTuple Production Scripts
==============

_Here's how to set up an appliance_

## Install Ubuntu 12.04

- Language will probably be English
- Location will probably be the United States
- Detect keyboard layout? No.
- Keyboard country is probably English US.
- Use eth0 as the Ethernet port if you have the option
- Make both the host name a lowercase version of the customer's CRM account name in dogfood
#### Full Name of User
- `xtadmin`
#### Username
- `xtadmin`
- Generate password using `openssl rand 6 | base64`

#### Encrypt Home Directory?
- No.

#### Timezone
- Set the correct timezone based on where the customer is

#### Disk Partition
- `Use the entire disk`

#### Write changes to disk
- `Yes`. This will begin the installation

#### HTTP Proxy
- The HTTP proxy information will almost always be "none", but this is a potential customization point

#### Software
- No automatic updates
- `OpenSSH Server` is the only software to install. Select using spacebar.

#### Install GRUB Bootloader
- `Yes`.
- Use the default bootloader device

#### Finish the installation
- `Continue`
- Make sure you have good internet access: `ping 8.8.8.8`

### Load the dependencies

- Put the certificate and key onto the appliance
- Also load the pilot database if we have one
- You can use a flash drive, or SCP, or whatever means you can to load these files
- You can put the files anywhere you want

### Bootstrap and install

- see https://github.com/xtuple/xtuple-server/wiki
