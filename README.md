# Threaded SSH Password Sprayer

Simple python3 script to spray a username and password (or ssh key) over ssh against a subnet. This repo currently includes two versions of the script:

1. ssh-sprayer-threaded2.py - this script first pings for live hosts and then performs the spray against live hosts...this script is only for password sprays
2. ssh_sprayer.py - this script does not ping first...it simply sprays against all hosts in a range over ssh. This script can spray for a password or for a private key.

It must be run with python3 and uses the paramiko library for ssh authentication. The script writes successful authentications to a file named "outfile.txt" in the current working directory.

first install the paramiko library:
pip3 install paramiko

Usages: 

1. python3 ssh-sprayer-threaded2.py 
Enter the username/password combo you want to check for, the target IP range, and the number of threads when prompted.

2. python3 sprayer-edited.py -u [username] (-p [password] OR -k <ssh_key>) -r [IP Range] -t [# of threads]
