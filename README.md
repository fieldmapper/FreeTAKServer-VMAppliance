# FreeTAKServer-VMAppliance

**FreeTAKServer Virtual Machine Appliance**

> This is a Debian GNU/Linux 10 FreeTAKServer (FTS) Virtual Machine Appliance. This VM appliance is geared towards end-users that would like to evaulate FTS ifcoin both TCP and SSL mode with minimal configuration from the end-user. Just import and run!

## What's Inside?

*   Debian GNU/Linux 10 - netinst
*   Python 3.7 w/ pip
*   Pre-configured FreeTAKServer 1.3.0.6 RC6

## What to do?

*   Download the latest `FTS-VMAppliance` image here - [http://bit.ly/ftsvmappliance](http://bit.ly/ftsvmappliance)
*   Download the default certificates specially built for this image.
*   Import and run the virtual machine image on your favorite VM emulator.
*   Take note of the IP address listed on the console. (You may need to login and check `ifconfig` if the IP address shows localhost. This VM is configured on VirtualBox attached to a `Bridged Adapter`. You may need to run `dhclient enp0s3` or manually configure the IP address in `/etc/network/interfaces`.

## First Start Notes, Comments:

*   Once appliance is booted up. Login to `fts` to change password.
*   The user `fts` has `sudo` privileges.
*   Depending on the VM emulator, there may be a delay on getting an IP address via DHCP. Resulting in an erroneous `Server IP` on the login screen. You can just run `dhclient (interfacename)` to get networking up and running.
*   All FTS-related process runs under the the user `fts` and the whole FreeTAKServer folder is owned by the `fts` user and group.

## Certificate Creation:

*   Server and Client Certificates were created by @lennacethemenace - [https://github.com/lennisthemenace/ATAK-Certs](https://github.com/lennisthemenace/ATAK-Certs)
*   `atakofthecerts.py` is already pre-loaded on `/home/fts/certs` and is sym-linked to the `/usr/local/lib/python3.x/dist-packages/FreeTAKServer/Certs` folder.
*   To create a new set of certificates please refer to the [https://github.com/lennisthemenace/ATAK-Certs](https://github.com/lennisthemenace/ATAK-Certs) documentation.

## Special thanks to...

*   The wonderful team over at FreeTAKServer ([https://github.com/FreeTAKTeam](https://github.com/FreeTAKTeam))
*   AFRL & TAK Product Center for creating and maintaining "The best Situational Awareness App that most have not heard about."
*   ATAK\_Release (civtak.org) for his "TAK evangelism" and efforts in getting ATAK released to the public, and the Google Play Store.
*   ATAK Discord and Reddit Administrators and Moderators for keeping the peace in our little corner of the Internet.
