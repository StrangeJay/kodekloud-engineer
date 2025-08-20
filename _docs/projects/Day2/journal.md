# Task

Temporary User Setup with Expiry

## Task Details

Create a temporary user that has an expiry date

### Solution

To create a temporary user with an expiry date in Linux, you can use the useradd command with the -e option. 

**`sudo useradd -e YYYY-MM-DD -m username`**

- Create a temporary user called jay that expires on August 10, 2025:

**`sudo useradd -e 2025-08-10 -m jay`**

> [!NOTE]
**`-e 2025-08-10`** sets the account expiration date. And **`-m`** creates a home directory for the user.

- Set a password: **`sudo passwd jay`**

- Confirm password: **`sudo chage -l jay`**