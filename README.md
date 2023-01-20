# SOLNEv1.1
SOftware for Lazy Network Engineers

This is a python program focused on facilitating repetetive tasks on major network deployments.

It currenlty ONLY performs backups on any Cisco IOS appliances. refer to the list of commands.

Program uses the same username, password for SSH and secret for all appliances. No current error handling, but it is planned.

The Backup function uses a text file with the list of IP Addresses, no need for commas after the IP address, it also works with hostnames DNS records if properly configured.
The text file can be named anything, no need to be named host.txt
eg
192.168.10.1
10.1.1.1
172.16.10.2


Program will create a folder called BACKUP[Current Date], and text file [Appliance Name]_[Current Date].txt for every appliances listed on the host text file.
