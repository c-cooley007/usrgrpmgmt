<h1>User & Group Management</h1>

<!-- ### [YouTube Demonstration](https://youtu.be/7eJexJVCqJo)
!-->
<h2>Description</h2>
This lab focuses on essential user management in Kali Linux, covering commands for creating, modifying, and deleting user accounts. You’ll learn to manage user settings, modify account details, and control system access through user locks and deletions. By the end, you'll be equipped with the skills to perform vital system administration tasks to ensure a secure and organized Linux environment.
<br />


<h2>Languages and Utilities Used</h2>

  - useradd
  - cat /etc/passwd
  - | grep
  - useradd -e YYYY-MM-DD 
  - chage -E YYYY-MM-DD
  - usermod
  - passwd 
  - su
  - sudo su
  - userdel


<h2>Environments Used </h2>

- Kali Linux

<h2>Lab Walk-Through:</h2>

<p align="center">
<b>useradd -D</b> :shows or sets the default settings applied when creating new user accounts: <br/>
<img src="https://i.imgur.com/sTvfJCF.png" height="80%" width="80%" alt="User & Group Management"/>
<br />
<br />
<b>useradd bob</b> : creates a new user named 'bob' with default settings. Ensure you are logged in as the root user:  <br/>
<img src="https://i.imgur.com/Y7pArSR.png" height="80%" width="80%" alt="User & Group Management"/>
<br />
<br />
<b>cat /etc/passwd</b> : Displays the contents of the /etc/passwd file, which contains information about all user accounts on the system: <br/>
<img src="https://i.imgur.com/rIumfoW.png" height="80%" width="80%" alt="User & Group Management"/>
<br />
<br />
<b>useradd -e YYYY-MM-DD james</b> : sets an expiration date for a new user 'james' in the format 'YYYY-MM-DD.' The account will be disabled after this date:  <br/>
<img src="https://i.imgur.com/x4o4gVF.png" height="80%" width="80%" alt="User & Group Management"/>
<br />
<br />
<b>chage -E YYYY-MM-DD bob</b> : sets an expiration date for the user 'bob' using the chage command, which manages user password aging. The account will be disabled after the specified date:  <br/>
<img src="https://i.imgur.com/ePEbghq.png" height="80%" width="80%" alt="User & Group Management"/>
<br />
<br />
<b>useradd -c "Jackson 5" Michael</b> : Creates a new user named 'Michael' with the comment 'Jackson 5,' 
  allowing the storage of additional user information. Then we verify the comments using <b>cat /etc/passwd | grep Michael</b> where you can see the new user with the comment:  <br/>
<img src="https://i.imgur.com/kns0W2N.png" height="80%" width="80%" alt="User & Group Management"/>
<br />
<br />
<b>usermod -l bob1 bob</b>: changes the username from 'bob' to 'bob1. Verified change and cat the /etc/passwd to see that bob is not listed as a user:  <br/>
<img src="https://i.imgur.com/Aaaxaf3.png" height="80%" width="80%" alt="User & Group Management"/>
<br />
<br />
<b>passwd bob1</b> : Prompts to set or change the password for the user 'bob1:  <br/>
<img src="https://i.imgur.com/R1SD59H.png" height="80%" width="80%" alt="User & Group Management"/>
<br />
<br />
<b> passwd -l bob1</b> : locks the account 'bob1,' preventing the user from logging in. Ensure you are logged in as the root user, as only root can lock other users' accounts: <br />
  <img src="https://i.imgur.com/WWA5hE6.png" height="80%" width="80%" alt="User & Group Management"/>
<br />
<br />
<b> su bob1 </b> : attempts to switch to the user 'bob1' in the current session, but will be denied due to the account being locked by the admin, 
  preventing login access. Ensure you're not logged in as root, as root has the privileges to override such restrictions: <br />
  <img src="https://i.imgur.com/z9t8Ghr.png" height="80%" width="80%" alt="User & Group Management"/>
<br />
<br />
<b>passwd -u bob1Z</b> : unlocks the account 'bob1,' re-enabling login access. Ensure you are logged in as the root user, as only root has the necessary privileges to unlock user accounts: <br />
 <img src="https://i.imgur.com/uqHRWDK.png" height="80%" width="80%" alt="User & Group Management"/>
<br />
<br />
<b>userdel bob1</b> : Deletes the user account 'bob1.' Note: This will only remove the user entry, not the home directory or files, unless additional options are specified. 
  Verify if the user 'bob1' still exists in the /etc/passwd file after deletion: <br />
 <img src="https://i.imgur.com/aTq2pbs.png" height="80%" width="80%" alt="User & Group Management"/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
