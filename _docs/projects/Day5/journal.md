# Task

SElinux Installation and Configuration

## Task Details

Install the necessary SELinux packages on the system but keep it in a disabled state.

### Solution

SELinux is generally included by default in distributions like RHEL, CentOS, and Fedora, so you usually just need to ensure the necessary packages are installed.

**Red Hat-based Systems (RHEL, CentOS, Fedora)**
On Red Hat-based systems, you can install the core SELinux policy and utilities using yum or dnf. SELinux is typically already installed, but if you need to add the policy packages, use this command:

**`sudo yum install policycoreutils selinux-policy-targeted`**

- Verify the installation with the **`sestatus`** command.
