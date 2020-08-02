# Useful SSH Commands

## Connecting to Server

### Basic Connections

`ssh user@192.168.1.1` - Basic connection

`ssh user@server_name` - Use DNS name 

`ssh user@server_name -p 1111` - Use different port 

`ssh user@server_name -i /path_to/pem_file` - Connect using file


## Generating Keys


`ssh-keygen` - Generate a basic key


## Config File

Set up a config file for regular SSH sessions


``` bash
Host my_server
    HostName 192.168.1.1
    User user_name
    Port 1111
    IdentityFile ~/.ssh/user_name.key
```

## Troubleshooting

`ssh -vvv -p 1111 user@192.168.1.1 date 2>&1` - Show verbose output on connection

`chmod 600 ~/.ssh/id_rsa` - Protect private key with correct permissions

`ssh-keygen -f .ssh/known_hosts -R  ip-or-hostname` - Delete an entry from known_hosts
