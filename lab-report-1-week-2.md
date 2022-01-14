Elena Tomson
---
Lab Report #1 Week 2

# Installing VScode
If you do not have VSCode already installed, install the proper verion for your computer [here](https://code.visualstudio.com/Download)

![Image](VSCode-Download.PNG)

Once you have VSCode, open it.
![Image](VSCode.png)

# Remotely Connecting

First, [Install-SSH](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse)
To remotely connect, type ssh and your username and your password when prompted.

*Note*: You will need to input your password whenever prompted until we set up the ssh key. 
![Sign-In](log-in.PNG)

Then you should see something resembling this
![Signed-In](signed-in.png)

# Trying Some Commands

From here, you can input an array of commands to the server: 

![CommandList](list-of-commands.PNG)

For example, "cd ~" goes to home directory, then ls lists the files there
![cd](cd-command.png)

# Moving Files with scp

Similarly to signing in, to copy a file from the client to the server, input the command "scp" followed by the file to be copied and then your username followed by :~/

![image](scp.PNG)

When I did this, the file copied over would print information about it's location when run.

![location](Where-am-I.png)
the first run is on the linux server and the second is on the windows client.

# Setting an SSH Key

First, you need to run "ssh-keygen" on the client.
Then enter the file name you want for your key, then leave the passphrase empty.

Then you need to make an ssh directory on the server.
![make-dir](make-dir.PNG)
Then copy the public key to the server using scp like 
scp /Users/joe/.ssh/id_rsa.pub cs15lwi22@ieng6.ucsd.edu:~/.ssh/authorized_keys

Make sure your path for your own private key is correct or it will fail like mine did.
![fail](bad-ssh.png)

# Optimizing Remote Running

To copy and run changes on the server quickly, type the scp and ssh commands for copying and then compiling and running the file, then use arrows to get up to them to rerun the program.

![faster](fast-changes.PNG)