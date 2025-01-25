# UFW Configuration Settings

## Default Rules
- Default incoming: DENY
- Default outgoing: ALLOW

## Allowed Ports
- Port 22 (SSH): Enabled for remote access
- Port 53 (DNS): Enabled for Pi-hole DNS queries

## Custom Rules
- SSH Login Attempts Limit: sudo ufw limit ssh
- ICMP (Ping): sudo ufw allow proto icmp

## Logging
- Logging Level: ON (default)
- View Logs: sudo tail -f /var/log/ufw.log
