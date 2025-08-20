# Task

Create a user with a non interactive shell on app server 1

## Solution

- ssh into App server i using the necessary credentials **`ssh username@app-server-1-ip`**.

- Create the user with a non interactive shell **`sudo useradd -s /usr/sbin/nologin newusername`**.

- verify by running the command **`getent passwd newusername`**.

