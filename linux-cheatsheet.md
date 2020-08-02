# Useful Linux Commands

### Processes / Troubleshooting

`ps aux | grep SEARCH_FOR_ME` - Find a process running with `SEARCH_FOR_ME` listed

`kill - 9 PID` - Kill a process ID. Get it using the `ps aux` command above

`ps -o etime= -p "31142"` - Show how long a process has been running 

`mysql -e "show full processlist\G" > processlist3.txt` - Export mysql processlist. Good for finding long running queries


### Misc 

`df -h` - Show human readable disk usage

`tar -zcvf archive.tar.gz directory/` - Zip up directory


### Directory

`du -h --max-depth=1 | sort -hr` - Sort by largest directory

`ln -sfr from_dir to_dir` - Create symlink 

`mkdir -p /folder1/folder2` - Recursively create directories


`grep newSearch /var/log/access-log | awk '{ print $1 }' | sort | uniq -c | sort -nr | head -n30` - Find most common occurrence in a file


### Finding / Filtering 

`echo */ | wc` - Find number of directories

`find . -size +10G -exec ls -lh {} \+` - Find files over 10Gb in a directory

`find -size +1M -delete` - Delete files over 1Mb in a directory

`find -type f -name '*find_and_delete_me*' -delete`

`find -type f -name '*find_and_delete_me[1-7]*'`

### SCP

`scp username@remote_host:file.txt /local_directory/` - Download a file from a remote server **TO** your machine

`scp -r local_directory username@remote_host:/some/remote/directory` - Upload a file **TO** remote machine

### File Operations

`> text_file.txt` - Empty out a text file
