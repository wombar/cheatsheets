# Rsync Cheatsheet

### Syntax

`rsync [ARGUMENTS] source_folder destination_folder` - Basic format of syntax

### Examples
Sync files **FROM** a remote server (recursively) to your local machine using SSH (private key specified) and a non-standard SSH port

`rsync -avzh -e "ssh -i /home/user/.ssh/id_rsa -p 2020" user@192.168.1.1:/home/user/ /putFilesHere/ --progress --cvs-exclude`


### Arguments

`-v` | `–verbose` - Verbose output

`-q` | `–quiet` - Suppress message output

`-a` | `–archive` - Archive files and directory while synchronizing ( -a equal to following options -rlptgoD)

`-r` | `–recursive` - Sync files and directories recursively

`-b` | `–backup` - Take the backup during synchronization

`-u`  | `–update` - Don’t copy the files from source to destination if destination files are newer

`-l` | `–links`- Copy symlinks as symlinks during the sync

`-n` | `–dry-run` - Perform a trial run without synchronization

`-e` | `–rsh=COMMAND` - Mention the remote shell to use in rsync

`-z` | `–compress` - Compress file data during the transfer

`-h` | `–human-readable` - Display the output numbers in a human-readable format

`–progress` - Show the sync progress during transfer
