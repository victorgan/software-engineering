# Forward Secrecy

> <- Back to [[Diffie-Hellman Key Exchange]]

The property that compromising long-term keys does not compromise past session keys. Achieved by using ephemeral keys for each session (ECDHE). Even if a server's private key is stolen, previously recorded encrypted traffic cannot be decrypted. Mandatory in TLS 1.3.

#cryptography #diffie-hellman #forward-secrecy
