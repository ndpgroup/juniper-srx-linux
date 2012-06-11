Juniper SRX Dynamic VPN client setup script
===========================================
James E. Flemer <james.flemer@ndpgroup.com>

June 10, 2012

Description
-----------
This script uses the Juniper Access Manager (JAM) web services to
download VPN settings from a Juniper SRX firewall (or other JunOS
device with Dynamic VPN support).  It is capable of writing the
settings out in the format used by network-manager-vpnc, and the
format used by plain vpnc.
 
Known Limitations
-----------------
 * Vpnc and network-manager-vpnc need patches to support Juniper
   SRX.  Hopefully these will be integrated upstream soon.
 * Plain vpnc doesn't have the ability to setup routes like
   network-manager.
 * The IKE and IPSec algorithms are not processed yet.  This
   should be trivial to add if needed.  (Add "debug 1" to the
   command line to get started.)

Future Enhancements
-------------------
 * Ideally, this capability would be directly integrated into the
   network-manager-vpnc GUI in some way (i.e. act a bit more like
   the windows JAM client.)

See Also
--------
 * vpnc: http://www.unix-ag.uni-kl.de/~massar/vpnc/
 * NetworkManager: http://projects.gnome.org/NetworkManager/
 * vpnc w/ Juniper SRX support: https://github.com/ndpgroup/vpnc
