# vm

This script makes it easier for Windows host to connect with Linux Hyper-V guest machines with the command:

    vm ssh
    
The guest machine is determined by running `arp -a` to determine the current IP address from the a saved MAC address.
The user is user may be prompted for the `SSH username` to login.
This script assumes a bash scripting environment ( e.g. git-bash ).

The full syntax is:

    vm [-select] [-login] ssh [sshoptions] [sshuser@] [sshparameters]
    
For example, one run the following commands against different users on the same VM:

    vm ssh user1@ ls
    vm ssh user2@ pwd
