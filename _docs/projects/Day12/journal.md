# Task

Linux Network Services

# Task Description

Our monitoring tool has reported an issue in Stratos Datacenter. One of our app servers has an issue, as its Apache service is not reachable on port 8084 (which is the Apache port). The service itself could be down, the firewall could be at fault, or something else could be causing the issue.

Use tools like telnet, netstat, etc. to find and fix the issue. Also make sure Apache is reachable from the jump host without compromising any security settings.

Once fixed, you can test the same using command curl http://stapp01:8083 command from jump host.

Note: Please do not try to alter the existing index.html code, as it will lead to task failure.

# Solution

## Option 1: The Preferred Solution

Instead of disabling the sendmail service, you can change the port Apache listens on. This allows you to fulfill the underlying goal of the task without compromising a potentially important system service. I recommend this approach for a real-world scenario. I changed the Apache port to 8084 and used that for my documentation. After which i redid the task and followed option 2.

## Option 2: The Required Solution
To pass the check that runs curl http://stapp01:8083 from the jump host, you must follow the instructions precisely. This means leaving the Apache port at its default setting and then stopping and disabling the sendmail service.

## Documentation

sudo iptables -L -n

sudo iptables -I INPUT -p tcp --dport 8084 -j ACCEPT

sudo service iptables save
