- Made a typo on setting IPV4 IP address. (Honest mistake)

- Didn't set both networks on HoST-ONLY adapter (Fixed)

- DHCP server - "Enable Server" should not be checked
	Reason: Enabling DHCP will randomly assign a IPv4 to both VMs, preventing you from having full control of the lab network

- If I like to use domain (required), Windows 10/11 MUST be Pro, as Home cannot join domains

- Doesn't seem like I can join domain as administrator, so I created "IT Admin user" created a password for the user
	Possible reason? : I may have set the password incorrectly, so I went to the main server and changed the password from their, afterwards I inserted the credentials for administrator and it work.

- Came across an issue where when setting shared folders I am not able to remove general User permission, to mend this ( 1 Solution) I changed the setting which disables inheritance
