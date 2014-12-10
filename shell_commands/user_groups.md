#### Shell Commands related to User's and Groups
##### Note: All commands run successfully in Ubuntu 14.04

1. who

2. whoami

3. groups <user_name>
See Which Groups Your Linux User Belongs To
When you are using a linux system, it’s useful to find out what groups you belong to, so you can understand whether you have access to files and directories. This is one of the simplest commands possible. I’m using Ubuntu linux, but this command should work on most varieties of linux.
If you don’t enter a username, it defaults to your own username. For instance:

geek@ubuntuServ:$ groups
geek adm dialout cdrom floppy audio dip video plugdev lpadmin scanner admin fuse

You can also check the groups for any other user, including root:

geek@ubuntuServ:$ groups root
root : root fuse

4. sudo cat /etc/group to see all groups

5. Add a new user:
sudo useradd <new_user_name>

6. Remove/Delete a user:
sudo userdel <existing_user_name>

7. Modify user:
usermod -l <new_username> <old_username>

8. Change the password for a user
sudo passwd <username>

9. Change the shell of user:
sudo chsh <username>

10. To change the details for a user (for example real name):
sudo chfn username

11. show id of user:
id <user_name>

If `user_name` is not specified, then it displays current user id.

12. Add a new group:
sudo groupadd <group_name>

13. Remove group:
sudo groupdel <group_name>

14. Add a user to an already existing group:
sudo usermod -G <group_name> <user_name>

15. Delete user from group:
sudo deluser <user_name> <group_name>

16. To show the last time each user logged into the system:
last

17. To enable 'Password Aging'(password expires after certain interval):
sudo chage <username>

* To list info of user's password aging: sudo chage --list <username>

18.