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

#### Port Forwarding

```
ssh -L 1234:localhost:80 myname@mycomputeripaddress
```

* `-L` enables port forwarding
* `local_socket:host:host_port`

**What**

SSH allows you to forward ports between a client & remote machine. This creates a 'tunnel' from your local machine to the remote server, allowing you to access their services.

* A secure connection to insecure services, e.g. connection to a home webserver
* To bypass firewalls, e.g. local cannot access email but remote can, therefore create tunnel between local and remote.

This allows you a secure connection to insecure services, or to bypass firewalls.

**How**

1. A socket listens to the local TCP port
2. When a connection is made to the local socket...
3. The connection is forwarded over SSH
4. The remote machine connects to the host port

**Why**

A remote may have access to services that your local machine does not. You can forward ports to create a 'tunnel' between your local machine and the remote, and thus the priviledged services.

> **Connecting to Insecure Service**
>
> You have a machine with an insecure service, e.g. a home webserver or security camera feed. SSH can be set up to securely connect to your home server, and then to that service.
>
> Stops you from exposing your insecure resource.
>
> **Bypassing Firewalls**
>
> Firewalls stop you from accessing your email, but you can access a remote that can bypass these firewalls. You can create a tunnel between your local machine and the remote, and then point your email client to the local machine _through the tunnel_ and onto the service.
>
> E.g. Access Aussie email from China through SSH tunnel

---

## SCP

```
scp <local-file> u6386433@partch.anu.edu.au:~/some-directory/
```



