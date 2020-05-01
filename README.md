# Delete-local-user-using-shell-script

This script makes use of various linux commands such as getopts, userdel, tar, chage etc. to perform a bunch of actions on the users passed in as the arguments. An account is disabled by default (using chage). If -d option is enabled, the account is permanently deleted. If -r option is enabled, the user's files are removed before deleting his account. If -a option is enabled, his entire data is backed up into the archives directory. The archives directory is not created by default and hence there's a check at the beginning of the script which takes care of the problem. All other edge cases such as root priveleges, modifying a system account etc. All the error related messages are dumped to STDERR and all the output from commands is dumped to /dev/null.

Commands used: tar, userdel, chage, getopts, shift, mkdir
