# SSH_Remote_Server_Setup
Setup a basic remote linux server and configure it to allow SSH

### Steps
- Created a remote Linux server on AWS
- After, created a Linux server on AWS to access the remote server
- Next, created the ssh keys in Linux server using 'ssh-keygen' command.
- Then, copied the contents from public key and pasted in the .ssh/authorized_keys file of remote server.
- Furthermore, connected using 'ssh -i user_name@remote_server_public_ip'. It's running successfully.
