# General Installation NotesA

## Kernel Version

3.10

## Text Consoles

* _Console 1_ Main text-mode installer console.
* _Console 2_ Shell.
* _Console 3_ Installation messages.
* _Console 4_ Storage messages.
* _Console 5_ Program messages.
* _Console 6_ Graphical installations.

## Software Selection

* _Minimal Install_ Basic RHEL OS.
* _Infrastructure Server_ Minimal plus basic network services.
* _File and Print Server_ Minimal plus file, print and storage services.
* _Basic Web Server_ Infrastructure plus Apache web server.
* _Virtualization Host_ Inftrastructure plus virtualization support.
* _Server with GUI_ Infrastructure with graphics support.

## Partioning

* LVM is used if automatic partitioning is selected.
* /boot must not be within an LVM volume group.
