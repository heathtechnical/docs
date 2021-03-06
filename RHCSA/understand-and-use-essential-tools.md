# Objectives

* Access a shell prompt and issue commands with correct syntax
* Use input-output redirection (>, >>, |, 2>, etc.)
* Use grep and regular expressions to analyze text
* Access remote systems using ssh
* Log in and switch users in multiuser targets
* Archive, compress, unpack, and uncompress files using tar, star, gzip, and bzip2
* Create and edit text files
* Create, delete, copy, and move files and directories
* Create hard and soft links
* List, set, and change standard ugo/rwx permissions
* Locate, read, and use system documentation including man, info, and files in /usr/share/doc

# Access a shell prompt and issue commands with correct syntax

Being able to bring up a shell and do this should satisfy this one:

    $ whoami

# Use input-output redirection (>, >>, |, 2>, etc.)

For the ones specified:

    $ grep http /etc/services > services.web
    $ grep https /etc/services >> services.web
    $ cat /etc/services | grep ftp
    $ find /etc 2> /dev/null > files.etc

And a few more:

    $ find /etc 2>&1 | grep "Permission denied"
    $ find /etc 1> files.etc.out 2> files.etc.err
    $ find /etc &> files.etc.merged
    $ find /etc 2>> files.etc.err.log
    $ cat > services.copy < /etc/services

We can even emulate a traditional open, read, close:

    $ cat /etc/services > file
    $ exec 3<> file
    $ grep http <&3
    $ exec 3>&-

# Archive, compress, unpack, and uncompress files using tar, star, gzip, and bzip2

SELinux attributes can be archived using star:

    $ star cvf etc.tar -xattr -H=exustar /etc

    $ Log in and switch users in multiuser targets

List logged in users with:

    $ w

Get last login times for all users with (utmp):

    $ lastlog

List historical logins and system reboots (from wtmp):

    $ last

List failed logins (from btmp):

    $ lastb
