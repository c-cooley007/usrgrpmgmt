<h1>User & Group Management</h1>

<!-- ### [YouTube Demonstration](https://youtu.be/7eJexJVCqJo)
!-->
<h2>Description</h2>
This lab focuses on essential user management in Kali Linux, covering commands for creating, modifying, and deleting user accounts. You’ll learn to manage user settings, modify account details, and control system access through user locks and deletions. By the end, you'll be equipped with the skills to perform vital system administration tasks to ensure a secure and organized Linux environment.
<br />


<h2>Languages and Utilities Used</h2>

  - <b> useradd -D </b>
  - <b> useradd </b>
  - <b> cat /etc/passwd  </b>
  - <b> cat /etc/passwd | grep </b> 
  - <b> useradd -e YYYY-MM-DD </b>
  - <b> chage -E YYYY-MM-DD </b>
  - <b> usermod -l </b>
  - <b>passwd </b>
  - <b> passwd -l </b>
  - <b> passwd -u </b>
  - <b> su </b>
  - <b> sudo su </b>
  - <b> userdel </b>


<h2>Environments Used </h2>

- <b>Kali Linux</b>

<h2>Program walk-through:</h2>

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
