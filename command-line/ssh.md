# SSH, Secure Shell

An SSH client is for \(securely\) logging into a remote machine and for executing commands on a remote machine.

It is intended to provide secure communication between two untrusted hosts over an insecure network.

#### Technical Details

1. The remote machine listens for connections on `Port 22`
2. The client connects to the server \(remote machine\)
3. A secret session key is agreed upon
4. Connection is made

#### Authorised Users

The `~/.ssh/authorized_keys` file holds a list of public keys that can log in as a user.

## Usage

```
ssh u6386433@partch.anu.edu.au
```



---

## SCP

```
scp <local-file> u6386433@partch.anu.edu.au:~/some-directory/
```





