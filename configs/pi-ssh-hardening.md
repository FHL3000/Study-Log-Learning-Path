# SSH Hardening Configuration

This markdown outlines the steps taken to harden SSH access for the Raspberry Pi in my home lab. These configurations are designed to enhance security and prevent unauthorized access.

---

## **1. Disable Root Login**
- Edited the SSH configuration file:
  ```plaintext
  /etc/ssh/sshd_config
  ```
- Changed the following line to disable root login:
  ```plaintext
  PermitRootLogin no
  ```
- Restarted the SSH service to apply changes:
  ```bash
  sudo systemctl restart ssh
  ```

---

## **2. Enable Key-Based Authentication**
- **Generated SSH Key Pair**:
  ```bash
  ssh-keygen -t rsa -b 4096
  ```
  - Saved the key pair in the default location: `~/.ssh/id_rsa`.
  - Optionally set a passphrase for additional security.

- **Copied Public Key to Raspberry Pi**:
  ```bash
  ssh-copy-id fhl3000@<Pi's_IP>
  ```
  - Replaced `<Pi's_IP>` with the actual IP address of the Raspberry Pi.

- **Tested Key-Based Login**:
  ```bash
  ssh fhl3000@<Pi's_IP>
  ```

- **Disabled Password Authentication** 
  Edited the SSH configuration file:
  ```plaintext
  /etc/ssh/sshd_config
  ```
  - Modified the following lines:
    ```plaintext
    PasswordAuthentication no
    PubkeyAuthentication yes
    ```
  - Restarted the SSH service:
    ```bash
    sudo systemctl restart ssh
    ```

---

## **3. Limit SSH Login Attempts**
- Added rate-limiting rules to prevent brute-force attacks:
  ```bash
  sudo nano /etc/fail2ban/jail.local
  ```
  - Added the following configuration:
    ```plaintext
    [sshd]
    enabled  = true
    port     = ssh
    filter   = sshd
    logpath  = /var/log/auth.log
    maxretry = 5
    bantime  = 10m
    findtime = 10m
    ```
- Restarted Fail2Ban to apply changes:
  ```bash
  sudo systemctl restart fail2ban
  ```

---

## **4. Restrict SSH Access by Subnet**
- Added UFW rule to allow SSH only from the local subnet:
  ```bash
  sudo ufw allow from 10.0.0.0/24 to any port 22
  ```

---

## **5. Test and Verify Configurations**
- **Login Tests**:
  - Verified key-based authentication works.
  - Ensured password login is disabled.

- **Fail2Ban Tests**:
  - Triggered repeated failed login attempts to confirm bans are enforced.
  - Monitored Fail2Ban logs:
    ```bash
    sudo tail -f /var/log/fail2ban.log
    ```

- **UFW Rules**:
  - Checked active rules:
    ```bash
    sudo ufw status numbered
    ```

---

## **Conclusion**
These SSH hardening steps significantly improve security for my Raspberry Pi, mitigating common vulnerabilities like brute-force attacks and unauthorized access. Key-based authentication, Fail2Ban, and subnet restrictions ensure a robust defense for remote access.
