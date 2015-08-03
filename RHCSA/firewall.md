# firewalld Basics

List zone definition:

    # firewall-cmd --list-all

Add allowed service temporarily and permanently:

    # firewall-cmd --add-service http
    # firewall-cmd --add-service http --permanent

Remove a service in the same way

    # firewall-cmd --remove-service http
    # firewall-cmd --remove-service http --permanent
