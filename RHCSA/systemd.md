# Basics

Start, stop, restart, reload, status:

    # systemctl start sshd
    # systemctl stop sshd
    # systemctl restart sshd
    # systemctl reload sshd
    # systemctl status sshd

# Journal

Get all logs:

    # journalctl

tail -f style:

    # journalctl -f

For a specific service, using time:

    # journalctl -u sshd --since yesterday
