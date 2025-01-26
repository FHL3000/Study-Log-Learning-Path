# Advanced UFW Configuration

This markdown documents the advanced UFW configuration implemented to secure and optimize the home lab network. These settings include ICMP rate-limiting, subnet restrictions, SSH hardening, and DNS management.

## ICMP Rules

```plaintext
# Allow ICMP echo-request only from the subnet
-A ufw-before-input -p icmp --icmp-type echo-request -s 10.0.0.0/24 -j ACCEPT

# Rate limit ICMP echo-request
-A ufw-before-input -p icmp --icmp-type echo-request -m limit --limit 3/sec --limit-burst 5 -j ACCEPT

# Allow ICMP diagnostic types
-A ufw-before-input -p icmp --icmp-type destination-unreachable -j ACCEPT
-A ufw-before-input -p icmp --icmp-type time-exceeded -j ACCEPT
-A ufw-before-input -p icmp --icmp-type parameter-problem -j ACCEPT
```

## SSH Rules

```plaintext
# Limit SSH attempts globally to prevent brute force attacks
-A ufw-before-input -p tcp --dport 22 -m conntrack --ctstate NEW -m recent --set --name SSH
-A ufw-before-input -p tcp --dport 22 -m conntrack --ctstate NEW -m recent --update --seconds 30 --hitcount 6 --name SSH -j DROP

# Allow SSH traffic within the subnet
-A ufw-before-input -p tcp --dport 22 -s 10.0.0.0/24 -j ACCEPT

# Default rate limit for SSH
22/tcp                     LIMIT IN    Anywhere
```

## Subnet Restrictions

```plaintext
# Allow traffic only from the 10.0.0.0/24 subnet
-A ufw-before-input -s 10.0.0.0/24 -j ACCEPT
```

## DNS Rules

```plaintext
# Allow DNS queries
-A ufw-before-input -p tcp --dport 53 -j ACCEPT
-A ufw-before-input -p udp --dport 53 -j ACCEPT

# Allow DNS outbound traffic
53                         ALLOW OUT   Anywhere
```

## HTTP/HTTPS Rules

```plaintext
# Allow outgoing web traffic
80                         ALLOW OUT   Anywhere
443                        ALLOW OUT   Anywhere

# Allow outgoing web traffic (IPv6)
80 (v6)                    ALLOW OUT   Anywhere (v6)
443 (v6)                   ALLOW OUT   Anywhere (v6)
```

## Default Policies

```plaintext
# Default UFW policies
Default incoming: DENY
Default outgoing: ALLOW
Default forward: DENY
```

## Additional Notes

- **Logging**: UFW logging is enabled to monitor allowed and denied traffic.
  ```plaintext
  sudo ufw logging on
  ```

- **Testing**: Connectivity and security settings are verified using:
  - `ping` to test ICMP rules.
  - `ssh` to confirm SSH access restrictions.
  - DNS queries to validate DNS rules.

## Next Steps
- Continue monitoring logs to ensure traffic behaves as expected.
- Expand or modify rules as needed to accommodate new services or devices.
