This is a guide to assist anyone that is attempting to use **Microsoft Visual Studio Code** to SSH/SFTP into an external server.

### Please follow the steps below in Order...
***Some common sense steps are missing... be smart...***

#### Step 1:
Download [**Visual Studio Code**](https://code.visualstudio.com/#alt-downloads)

#### Step 2:
**A:** Go to the **Extentions** tab as seen in image below.
**B:** Type in **Remote - SSH** in the search bar as seen in image below.
![d1a00a48-8df9-45c2-92fd-0b081661afa8-image.png](/assets/uploads/files/1580674665827-d1a00a48-8df9-45c2-92fd-0b081661afa8-image.png) 


#### Step 3: 
Click **Install**  This will promt dependiences to be installed so don't rush.
![a3939ccf-d56f-4dd4-b785-6e2db3ad6abd-image.png](/assets/uploads/files/1580674773251-a3939ccf-d56f-4dd4-b785-6e2db3ad6abd-image.png) 

#### Step 4: 
Setting up the config on this client is super easy and makes SFTP completely replaceable.
**Step 5.A** hit **F1** to pull up the command line in **Visual Studio Code**
**Step 4.B** type **Remote** and click **Remote-SSH: Open Configuration File...**
![9cbc3a5f-8696-4f2c-aefb-6c5ac0011dea-image.png](/assets/uploads/files/1580675048617-9cbc3a5f-8696-4f2c-aefb-6c5ac0011dea-image.png) 
**Step 4.C** You will be prompted to select your .ssh file location.  Don't worry.. If you don't have a config it will create one.
![0fb6a753-36e3-48cc-934c-ea527022b242-image.png](/assets/uploads/files/1580675163138-0fb6a753-36e3-48cc-934c-ea527022b242-image.png) 
**Step 4.D**  Adding your info to Config.
Follow the lines below and hit Save...
```
Host ipaddress
  HostName ip or hostname
  User username
  ForwardAgent yes
  IdentityFile C:\Users\[%USER%]\Documents\xsvCommunity\Keys\googlecloud
```



#### Things to NOTE

It is generally not a good idea to run VS Code as sudo. Instead change the permission for the directory.

You can change the ownership of the directory so that you can open it without needing root privileges.

```
$ sudo chown -R <user-name> <directory-name>
```
