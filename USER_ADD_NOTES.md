# Adding Users
useradd "USERNAME"

# Creates the user
passwd "USERNAME"

# Set the password
If no password set, cannot login.

Where the user information lives
/etc/passwd
Does not contain the password
greg:x:561:561:Greg W:/home/greg:/bin/bash
Username, password, uid, gid, comment, home directory, default shell
/etc/shadow
user:$6$BUT3hIub$JjoOhlK0:14478:0:99999:7:::

# The following are what each field represents, separated by a ":"

 * Username
 * Version of cipher - separated by a "$"
 * Encrypted password* - separated by a "$"
 * Salt* - separated by a "$"
 * Days since epoch of last password change
 * Days until change allowed
 * Days before change required
 * Days warning for expiration
 * Days before account inactive
 * Days since Epoch when account expires
 * Reserved
 * Groups
 * Groups are specified in /etc/group
 * EXAMPLE: safes:*:500:williams, jones

# The following are what each field represents, separated by a ":"

 * Group name
 * Password, if exists
 * Group ID
 * Group users
# Process for creating a user from start to finish : -
 * useradd greg
 * passwd greg
 * mkdir /home/greg
 * chown greg:greg /home/greg
 * vipw – modify default shell to what ever
 * /etc/adduser.conf – modify default parameters … or … specify different flags on useradd
