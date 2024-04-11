# root-pass-configuration

```bash
sudo sed -i 's/#PermitRootLogin prohibit-password/PermitRootLogin yes/' /etc/ssh/sshd_config && sudo systemctl restart ssh && sudo passwd
```

wuth this you modify the SSH configuration to allow root login, restart the SSH service, and change the root password. Let's break down each part of the command:

1.
" **sudo sed -i 's/#PermitRootLogin prohibit-password/PermitRootLogin yes/' /etc/ssh/sshd_config**": This command uses "**sed**" to edit the "**/etc/ssh/sshd_config**" file. It replaces the line "**#PermitRootLogin prohibit-password**" with "**PermitRootLogin yes**". This effectively allows root login via SSH.

2.
"**sudo systemctl restart ssh**": This command restarts the SSH service to apply the changes made to the configuration file.

3.
"**sudo passwd**": This command prompts you to enter a new password for the root user.

Make sure you understand the implications of enabling root login over SSH, as it can pose security risks. Additionally, always ensure you have a strong password for the root user.
