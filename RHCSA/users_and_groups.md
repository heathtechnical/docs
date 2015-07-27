# /etc/passwd

user:password:uid:gid:gecos:home:shell

password can be one of:

 * Encrypted password
 * 'x' -> Shadow file
 * '*' -> Account disabled

# /etc/shadow

user:password:lastchg:mindays:maxdays:warndays:inactivedays:disableddays:unused

 * password field starting ! -> Account locked
 * Epoch days since last password change
 * Min days before password change
 * Max days before password change
 * Number of days user will get password change warnings
 * Max days of user inactivity
 * Epoch day account expires

Can be changed using _chage_.

# /etc/group

user:password:gid:member1,memberN

Set a password using _gpasswd_ to allow non-members to be able to _newgrp_ to the group.

# /etc/gshadow

user:password:admins:members

 * password field: '!' -> disable _newgrp_ access, '!!' disable _newgrp_ also indicates
   group password has never been set
 * admins: list of users that can add/remove users
 * members list
