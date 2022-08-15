# Readings: API Deployment

## Django Settings Best Practices
Setting Configuration: Different Approaches

> settings_local.py
> Separate settings file for each environment
> Environment variables
> 12 Factors
> django-environ

Django Settings: Best practices

- Keep settings in environment variables.
- Write default values for production configuration (excluding secret keys and tokens).
- Don’t hardcode sensitive settings, and don’t put them in VCS.
- Split settings into groups: Django, third-party, project.
- Follow naming conventions for custom (project) settings.


## SSH 

### What Is SSH?

SSH, or Secure Shell Protocol, is a remote administration protocol that allows users to access, control, and modify their remote servers over the internet.

### How Does SSH Work

The most popular SSH client is PuTTY.

### Understanding Different Encryption Techniques

The significant advantage offered by SSH over its predecessors is the use of encryption to ensure a secure transfer of information between the host and the client. Host refers to the remote server you are trying to access, while the client is the computer you are using to access the host. There are three different encryption technologies used by SSH:
- Symmetrical encryption
- Asymmetrical encryption
- Hashing

### How Does SSH Work With These Encryption Techniques

The way SSH works is by making use of a client-server model to allow for authentication of two remote systems and encryption of the data that passes between them.

### Session Encryption Negotiation

When a client tries to connect to the server via TCP, the server presents the encryption protocols and respective versions that it supports. If the client has a similar matching pair of a protocol and version, an agreement is reached and the connection is started with the accepted protocol. The server also uses an asymmetric public key which the client can use to verify the authenticity of the host.


### Authenticating the User

The final stage before the user is granted access to the server is authenticating his/her credentials. For this, most SSH users use a password. The user is asked to enter the username, followed by the password. These credentials securely pass through the symmetrically encrypted tunnel, so there is no chance of them being captured by a third party.

