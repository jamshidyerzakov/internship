## Troubleshooting ssh connection
### By checking below steps we can can find the problem 
* Be sure sshd service in the server side is active working and listening in 22 port (systemctl status sshd)
* Be sure that you specified the correct port if it's changed in /etc/sshd/sshd_config
* Be sure that the username and ip address is correct - no typos
* Be sure that the password is correct - password auth
* Be sure that you are using correct key (private key) with correct flags (-i) and it has correct permissions (read only) - pub key auth
* If it's pub key auth make sure server `public key` (remote server .pub file) is in `authorized_keys` (.ssh/authorized_keys in remote server)
* Be sure that you are using correct path to the `private key` ( `ssh -i absolute/relative_path user@remote_ip -p 22(or other if it's changed)` 
