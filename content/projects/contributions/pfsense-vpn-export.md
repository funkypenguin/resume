{
    "title":"pfSense VPN export naming",
    "link":"https://github.com/pfsense/pfsense-packages/pull/872",
    "image":"/img/pfsense_openvpn_export.jpg",
    "description":"I submitted a PR to the pfsense-packages team to simplify the way OpenVPN configs are exported",
    "tags":["pfSense"],
    "weight":"5",
    "featured":true,
    "sitemap": {"priority" : "0.8"}
}

At [Prophecy](http://www.prophecy.net.nz), we use pfSense's OpenVPN capabilities to provide remote access for staff and customers. It's always bothered me how the exported VPN config is named ```<device name>-<port>-<certificate name>.ovpn```, for example **firewall3.us.global.becausimbatman.com-1194-brucewayne.ovpn**, since this is what the VPN client on Mac/Windows will forever call this VPN.

I submitted a simple [PR](https://github.com/pfsense/pfsense-packages/pull/872) to allow the exported package to be optionally named for the VPN server name (_i.e. "Office"_) instead, which I reasoned would make supporting my users easier.

Unfortunately the repo owners were slow to respond, and by the time the PR was ready to merge, a new version of the pfsense package was in the works (_requiring a redo_), and the PR was closed without consultation by the repo owner.
