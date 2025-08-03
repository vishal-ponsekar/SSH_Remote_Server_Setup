# SSH_Remote_Server_Setup
Set up a basic remote Linux server and configure it to allow SSH.

### Steps
- Created a remote Linux server on AWS.
- After, created another Linux server on AWS to access the remote server.
- Next, created two new SSH key pairs in the Linux server using the 'ssh-keygen' command.
- Then, copied the contents from the public key of the SSH key pairs and pasted them in the .ssh/authorized_keys file of the remote server.
- Furthermore, connected using the 'ssh -i .ssh/<key_name> user_name@remote_server_public_ip' command.
- And I give different names and passphrases to ensure both keys are working or not.
- I tried to connect with both keys. It's connected successfully.
- To connect to the remote server using a simple command like 'ssh \<alias\>', I created a file called config on the Linux server.
- After, added a block for the remote server using the following format.
```bash
Host <alias>
    HostName <server-address-or-IP>
    User <username>
    IdentityFile ~/.ssh/<private-key>
```
**Example**
  ```bash
  Host dev1
        	HostName 13.204.79.204
        	User ubuntu
        	IdentityFile ~/.ssh/id_rsa
  ```
- Next, I tried to connect like **ssh dev1** from the Linux server. It's connected successfully.
- And, I added another block with another key pair location and different name. That's also connected successfully.

### Project Description URL
https://roadmap.sh/projects/ssh-remote-server-setup
