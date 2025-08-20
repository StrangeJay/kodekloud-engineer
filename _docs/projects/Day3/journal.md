# Task

Secure Root SSH Access

## Task Details

Following security audits, the xFusionCorp Industries security team has rolled out new protocols, including the restriction of direct root SSH login.


Your task is to disable direct SSH root login on all app servers within the Stratos Datacenter.

### Solution

To disable direct SSH root login on all app servers, you'll need to update the SSH configuration file on each server and restart the SSH service. Here's how to do it step-by-step.

- SSH into each App server **`ssh user@stapp01`**

> [!NOTE]
(Repeat for stapp02, etc.)

- Edit the SSH Configuration File.

- Open /etc/ssh/sshd_config with a text editor (e.g., nano or vim) by running: **`sudo nano /etc/ssh/sshd_config`**.

- Find and Modify This Line. Change **`#PermitRootLogin yes`** to **`PermitRootLogin no`**.

> [!NOTE]
If the line is commented (#), uncomment it and set to no.

- Restart SSH Service: **`sudo systemctl restart sshd`**.

- Test that root SSH access is blocked: **`ssh root@app-server-1`**

You should see an error that says **"Permission denied, please try again."**

> [!NOTE]
This can also be done automatically with a bash script.
