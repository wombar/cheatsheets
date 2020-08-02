# Useful SSH Commands

## Connecting to Server

### Basic Connections

`ssh user@192.168.1.1` - Basic connection

`ssh user@server_name` - Use DNS name 

`ssh user@server_name -p 1111` - Use different port 


## Generating Keys


`ssh-keygen` - Generate a basic key


## Troubleshooting

`ssh -vvv -p 1111 user@192.168.1.1 date 2>&1` - Show verbose output on connection

`chmod 600 ~/.ssh/id_rsa` - Protect private key with correct permissions


