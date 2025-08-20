# Task
Script Execution Permission

## Task Details

In a bid to automate backup processes, the xFusionCorp Industries sysadmin team has developed a new bash script named xfusioncorp.sh. While the script has been distributed to all necessary servers, it lacks executable permissions on App Server 1 within the Stratos Datacenter.


Your task is to grant executable permissions to the /tmp/xfusioncorp.sh script on App Server 1. Additionally, ensure that all users have the capability to execute it.

### Solution

- ssh into app server 1: **`ssh tony@stapp01`**.

- To grant executable permissions to a file for all users, you can use the chmod command.

**`chmod 755 /tmp/xfusioncorp.sh`**

> [!NOTE]
The number 7 for the owner grants read, write, and execute permissions. The numbers 5 for the group and 5 for others grant read and execute permissions.

- You can verify the permissions using the **`ls -l /tmp/xfusioncorp.sh`** command. The output should show the execute permission **`(x)`** for all user categories.

