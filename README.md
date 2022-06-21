This repo is the infrastructure-as-code for my home media server.

It's based primarily on docker-compose but using the fantastic [DockSTARTer](https://dockstarter.com) project.

# VPN Configuration
For Private Internet Access and the qbittorrentvpn container.
- Ensure docker compose .env file has blank values for `VPN_PASS` and `VPN_USER`
- Log into PIA and download a `.ovpn` file into the dockstarter `VPN_OVPNDIR` folder
- This file should have a line `auth-user-pass credentials.conf`
- `credentials.conf` should exist beside the file .ovpn file and have:
```
<pia username>
<pia password>
```
- Test with [https://www.top10vpn.com/tools/do-i-leak/](https://www.top10vpn.com/tools/do-i-leak/)
