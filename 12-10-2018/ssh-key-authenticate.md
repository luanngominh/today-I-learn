# SSH Key Authentication

### Create ssh key
Create key for each user, I use rsa algorithm, key size 2048 bits <br>
`ssh-keygen -t rsa -b 2048`
This will create two file, one have `.pub` prefix. File has `.pub` prefix is public key, we will move it to $HOME/.ssh <br>
For instance, my public key is id_rsa.pub and private key is id_rsa. I change name id_rsa to id_rsa.pem
### Move public key to $HOME/.ssh
`mv id_rsa $HOME/.ssh/authorized_keys`

### Transfer private key for user and login
`ssh -i id_rsa.pem username@host`