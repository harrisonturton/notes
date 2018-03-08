# SSH

SSH is a network protocol for operating securely over an insecure network to an insecure host.

An **SSH Client **is a program for logging into and executing commands on a remote machine.

### Authentication

SSH uses a Client-Server model.

* **Server** on remote machine** listens to Port 22 **for client connections.
* When a client connects, a secret** session key** is agreed upon.
  * This session key is used for encrypting communication between client/server.
  * This key is never passed between client/server. **Diffie-Hellman approach **is used.

SSH can use a number of authentication approaches. The main ones are:

* Password-based authentication \(if the remote machine allows this\)
* Public key authentication

**Password Authentication**

Strengths

* Simple -- don't need to share/maintain keys
* People already have passwords

Weaknesses

* Can be forgotten
* Same password for different systems \(Bad!\)
* Can be guessed

**Public-Key Authentication**

PK Authentication provides you with something you **know **and something you **have** -- the pass-phrase and the encrypted private key. This is a convenient and secure technique.

Great in all places but:

* Server cannot check that strong pass-phrases are used
* If someone can alter `authorized_keys` file, they may insert an extra one

### Symmetric-Key Cryptography

The same key is used for encryption & decryption. Common approaches are DES, 3DES, AES, and TwoFish.

**Problem.** How are keys shared over an insecure channel? The \_Diffie-Hellman-Merkle \_key exchange scheme.

**Diffie-Hellman-Merkle Key Exchange Scheme**

1. Assume the numbers `5` and `7` are public.
2. Alice\_ \_thinks of a random number, e.g. `4`. This is \_not \_shared. She calculates $$5^4\text{ mod } 7=2$$.
3. She sends this result `2` over the insecure network, to Bob.
4. Bob also thinks of an \(unshared\) random number, e.g. `3`, and calculates $$5^3\text{ mod }7=6$$.
5. He sends this result `6` over the insecure network, to Alice.
6. Now **Alice has received a 6. **She calculates the secret key: $$6^4\text{ mod }7=1$$.
7. Now **Bob has received a 2. **He calculates the secret key: $$2^3\text{ mod }7=1$$

Someone watching will see the values `5`, `7`, `2` and `6`. They will not be able to construct the secret key from these values.

### Asymmetric-Key Cryptography

Different keys are used for encryption & decryption. A common approach is RSA.

### Tunneling / Port-Forwarding





