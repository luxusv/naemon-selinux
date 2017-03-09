# naemon-selinux
Selinux policies for naemon and thruk

# Description
Selinux policies written for naemon. These policies create some new filecontexts and allow httpd access to these folders and files.
When only using thruk it's enough to only build and install the thruk policies.

## Dependencies
selinux-policy-devel

## Installation
clone the repository
cd naemon
make -f /usr/share/selinux/devel/Makefile
semodule -i naemon.pp
cd ../thruk
make -f /usr/share/selinux/devel/Makefile
semodule -i thruk.pp
restorecon -R -v /
