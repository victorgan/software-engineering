# 08 — Security MOC

> ← Back to [[Software Engineering - Map of Content]]

Protecting systems, data, and users from harm. Security is not a feature — it's a property of the system that must be woven into every layer.

---

## [[Cryptography]]

### Hashing
- **Concept** — One-way function, fixed-size output, deterministic
- **Properties** — Collision resistance, pre-image resistance, avalanche effect
- **Algorithms** — SHA-256, SHA-3, BLAKE2, BLAKE3
- **Password Hashing** — bcrypt, scrypt, Argon2 (slow by design, salted, adaptive)
- **HMAC** — Hash-based Message Authentication Code, verify integrity + authenticity
- **Use Cases** — Password storage, data integrity, digital signatures, deduplication

### Symmetric Encryption
- **Concept** — Same key for encryption and decryption
- **AES (Advanced Encryption Standard)** — AES-128, AES-256, block cipher
- **Block Cipher Modes** — CBC, CTR, GCM (authenticated encryption)
- **ChaCha20-Poly1305** — Stream cipher, alternative to AES-GCM, used in TLS
- **Use Cases** — Data at rest, disk encryption, database encryption

### Asymmetric Encryption (Public Key)
- **Concept** — Key pair: public key (encrypt) + private key (decrypt)
- **RSA** — Based on factoring large primes, 2048+ bit keys
- **Elliptic Curve Cryptography (ECC)** — Smaller keys, same security (Ed25519, P-256)
- **Diffie-Hellman Key Exchange** — Establish shared secret over insecure channel
- **Use Cases** — TLS handshake, SSH, email encryption (PGP/GPG), digital signatures

### Digital Signatures
- **Concept** — Prove authenticity and integrity using private key
- **Process** — Hash message → sign hash with private key → verify with public key
- **Algorithms** — RSA-PSS, ECDSA, Ed25519
- **Use Cases** — Code signing, JWT signing, certificate signing, document signing

### TLS/SSL
- **TLS Handshake** — Client Hello, Server Hello, certificate exchange, key exchange
- **TLS 1.3** — Reduced round trips (1-RTT, 0-RTT), removed weak cipher suites
- **Certificates** — X.509, Certificate Authorities (CAs), chain of trust
- **Let's Encrypt** — Free, automated certificate issuance (ACME protocol)
- **Certificate Pinning** — Pin expected certificate/public key (mobile apps)
- **mTLS (Mutual TLS)** — Both sides authenticate (used in [[Distributed Systems|service mesh]])

### PKI (Public Key Infrastructure)
- **Certificate Authorities** — Root CAs, intermediate CAs, certificate chain
- **Certificate Lifecycle** — Issuance, renewal, revocation (CRL, OCSP)
- **Key Management** — Key rotation, key escrow, HSMs (Hardware Security Modules)

---

## [[Authentication and Authorization]]

### Authentication (Who are you?)
- **Password-Based** — Hashed + salted storage, strength requirements
- **Multi-Factor Authentication (MFA)** — Something you know + have + are
- **TOTP** — Time-based one-time passwords (Google Authenticator, Authy)
- **WebAuthn / FIDO2 / Passkeys** — Passwordless, hardware-backed, phishing resistant
- **Biometrics** — Fingerprint, face recognition (local verification)
- **Magic Links** — Passwordless email-based authentication
- **SSO (Single Sign-On)** — One login across multiple services

### OAuth 2.0
- **Roles** — Resource Owner, Client, Authorization Server, Resource Server
- **Grant Types** — Authorization Code (+ PKCE), Client Credentials, Device Code
- **Deprecated Grants** — Implicit (replaced by Auth Code + PKCE), Resource Owner Password
- **Access Tokens** — Short-lived, bearer tokens, scopes
- **Refresh Tokens** — Long-lived, used to obtain new access tokens
- **Token Revocation** — Invalidating tokens before expiry

### OpenID Connect (OIDC)
- **Concept** — Identity layer on top of OAuth 2.0
- **ID Token** — JWT containing user claims (sub, email, name)
- **UserInfo Endpoint** — Retrieve additional user information
- **Discovery** — .well-known/openid-configuration

### JWT (JSON Web Tokens)
- **Structure** — Header.Payload.Signature (base64url encoded)
- **Claims** — iss, sub, aud, exp, iat, nbf, custom claims
- **Signing** — HMAC (symmetric), RSA/ECDSA (asymmetric)
- **Validation** — Verify signature, check expiry, validate issuer/audience
- **Security Concerns** — Don't store secrets, set short expiry, use asymmetric signing
- **JWE** — Encrypted JWTs for confidential claims

### Authorization (What can you do?)
- **RBAC (Role-Based Access Control)** — Users → Roles → Permissions
- **ABAC (Attribute-Based Access Control)** — Policies based on user/resource/environment attributes
- **ReBAC (Relationship-Based Access Control)** — Based on relationships between entities (Google Zanzibar)
- **ACL (Access Control Lists)** — Per-resource permission lists
- **Policy Engines** — OPA (Open Policy Agent), Cedar, Casbin
- **Authorization Patterns** — Centralized vs distributed, policy-as-code

### Identity Providers
- **Auth0 / Okta** — Identity-as-a-Service
- **Keycloak** — Open-source identity and access management
- **AWS Cognito** — Managed auth for AWS apps
- **Firebase Auth** — Google's managed auth

---

## [[Application Security]]

### OWASP Top 10 (2021)
1. **Broken Access Control** — Missing authorization checks, IDOR, privilege escalation
2. **Cryptographic Failures** — Weak encryption, cleartext transmission, hardcoded secrets
3. **Injection** — SQL injection, NoSQL injection, OS command injection, LDAP injection
4. **Insecure Design** — Missing security requirements, threat modeling gaps
5. **Security Misconfiguration** — Default credentials, unnecessary features, verbose errors
6. **Vulnerable Components** — Outdated dependencies, known CVEs
7. **Authentication Failures** — Weak passwords, credential stuffing, session fixation
8. **Data Integrity Failures** — Insecure deserialization, untrusted CI/CD pipelines
9. **Logging & Monitoring Failures** — Insufficient logging, no alerting (see [[Observability]])
10. **Server-Side Request Forgery (SSRF)** — Server makes requests to internal resources

### Common Vulnerabilities
- **Cross-Site Scripting (XSS)** — Reflected, Stored, DOM-based; mitigation: output encoding, CSP
- **Cross-Site Request Forgery (CSRF)** — Forged requests from authenticated user; mitigation: CSRF tokens, SameSite cookies
- **SQL Injection** — Untrusted input in SQL queries; mitigation: parameterized queries, ORM
- **SSRF** — Server-side requests to internal services; mitigation: allowlists, network segmentation
- **Path Traversal** — Accessing files outside intended directory; mitigation: input validation, chroot
- **Insecure Deserialization** — Arbitrary code execution via crafted serialized data
- **Clickjacking** — Invisible iframe overlay; mitigation: X-Frame-Options, CSP frame-ancestors

### Secure Development Practices
- **Input Validation** — Allowlisting, type checking, length limits, sanitization
- **Output Encoding** — Context-appropriate encoding (HTML, URL, JavaScript, SQL)
- **Principle of Least Privilege** — Minimum necessary permissions
- **Defense in Depth** — Multiple layers of security controls
- **Secure Defaults** — Deny by default, opt-in for access
- **Security Headers** — CSP, HSTS, X-Content-Type-Options, Referrer-Policy, Permissions-Policy
- **Dependency Scanning** — Dependabot, Snyk, npm audit, OWASP Dependency-Check
- **SAST (Static Application Security Testing)** — Code analysis for vulnerabilities (Semgrep, SonarQube)
- **DAST (Dynamic Application Security Testing)** — Runtime vulnerability scanning (OWASP ZAP, Burp Suite)

### Threat Modeling
- **STRIDE** — Spoofing, Tampering, Repudiation, Information Disclosure, Denial of Service, Elevation of Privilege
- **Attack Trees** — Model attacker goals and methods
- **Data Flow Diagrams** — Map trust boundaries, data flows, entry points
- **Risk Assessment** — Likelihood × Impact, prioritize mitigations

---

## [[Infrastructure Security]]

### Network Security
- **Firewalls** — Network-level and application-level (WAF), security groups
- **Network Segmentation** — VPCs, subnets, DMZ, microsegmentation
- **Zero Trust Architecture** — Never trust, always verify, regardless of network location
- **VPN / WireGuard** — Encrypted tunnels for secure remote access
- **DDoS Protection** — Rate limiting, CloudFlare, AWS Shield, traffic scrubbing

### Secrets Management
- **Principles** — Never hardcode secrets, rotate regularly, least privilege
- **Tools** — HashiCorp Vault, AWS Secrets Manager, Azure Key Vault, SOPS
- **Environment Variables** — Better than hardcoding, but limited (no rotation, no audit)
- **Secrets in CI/CD** — GitHub Actions secrets, masked variables, OIDC for cloud auth

### Container Security
- **Image Security** — Minimal base images (distroless, Alpine), vulnerability scanning (Trivy, Snyk)
- **Runtime Security** — Read-only filesystems, non-root users, seccomp profiles, AppArmor
- **Supply Chain** — Image signing (cosign, Notary), SBOM (Software Bill of Materials)
- **Kubernetes Security** — RBAC, network policies, pod security standards, admission controllers

### Data Protection
- **Encryption at Rest** — Disk encryption, database encryption, key management
- **Encryption in Transit** — TLS everywhere, mTLS for internal traffic
- **Data Classification** — Public, internal, confidential, restricted
- **Data Retention** — Retention policies, right to deletion (GDPR), data lifecycle
- **Backup Security** — Encrypted backups, tested restores, offsite storage

---

## [[Supply Chain Security]]

### Software Supply Chain
- **Dependency Vulnerabilities** — Transitive dependencies, CVE databases, automated scanning
- **Dependency Pinning** — Lock files (package-lock.json, Pipfile.lock, go.sum), reproducible builds
- **SLSA Framework (Supply-chain Levels for Software Artifacts)** — Levels 1-4 of build integrity, provenance attestation
- **SBOM (Software Bill of Materials)** — CycloneDX, SPDX formats; know what's in your software
- **Artifact Signing** — Sigstore, cosign, Notary — verify artifact integrity and provenance
- **Typosquatting** — Malicious packages with similar names on registries (npm, PyPI)
- **Dependency Confusion** — Private package names registered publicly, attacker's version installed

### CI/CD Security
- **Pipeline Hardening** — Least privilege for CI, no long-lived secrets, ephemeral runners
- **OIDC for Cloud Auth** — Short-lived tokens instead of static credentials (GitHub Actions → AWS/GCP)
- **Code Signing** — Sign commits (GPG), sign artifacts, verify before deploy
- **Immutable Artifacts** — Build once, promote through environments, never rebuild (see [[CI-CD]])

---

## [[Compliance & Privacy]]

### Regulatory Frameworks
- **GDPR (EU)** — Data subject rights (access, erasure, portability), DPO, consent, breach notification within 72h
- **CCPA/CPRA (California)** — Consumer privacy rights, opt-out of data sale, right to know
- **SOC 2** — Trust service criteria: security, availability, processing integrity, confidentiality, privacy
- **HIPAA (US Healthcare)** — Protected Health Information (PHI), BAA agreements, encryption requirements
- **PCI-DSS** — Payment card data handling, network segmentation, encryption, regular assessments
- **ISO 27001** — Information security management system (ISMS), risk-based approach

### Privacy Engineering
- **Privacy by Design** — Build privacy into architecture from the start, not as an afterthought
- **Data Minimization** — Collect only what you need, retain only as long as necessary
- **Anonymization vs Pseudonymization** — True anonymization is irreversible; pseudonymization is reversible with a key
- **Differential Privacy** — Mathematical guarantee that individual data points don't significantly affect output
- **Consent Management** — Granular consent, easy withdrawal, consent records
- **Right to Erasure** — Soft delete vs hard delete, propagation to backups, third-party data processors

---

## [[Security Operations]]

### Vulnerability Management
- **CVE Tracking** — Common Vulnerabilities and Exposures, NVD database, CVSS scoring
- **Patch Management** — Prioritize by severity (CVSS), apply within SLA, automated patching where possible
- **Bug Bounty Programs** — Crowdsourced vulnerability discovery (HackerOne, Bugcrowd)
- **Responsible Disclosure** — Coordinated vulnerability disclosure, 90-day deadlines

### Security Monitoring
- **SIEM (Security Information and Event Management)** — Splunk, Sentinel, Elastic Security — centralized security event analysis
- **IDS/IPS** — Intrusion detection/prevention systems, network-based and host-based
- **Honeypots** — Decoy systems to detect and study attackers
- **Security Logging** — Authentication events, authorization failures, admin actions, data access (see [[Observability]])

### Penetration Testing
- **Types** — Black box (no knowledge), white box (full access), gray box (partial)
- **Methodology** — Reconnaissance → scanning → exploitation → post-exploitation → reporting
- **Tools** — Burp Suite, OWASP ZAP, Nmap, Metasploit, Nuclei
- **Frequency** — Annual at minimum, after major changes, for compliance requirements
- **Red Team vs Blue Team** — Red team: attack simulation. Blue team: defense and detection. Purple team: collaborative improvement.

---

#security #cryptography #authentication #owasp #supply-chain #compliance #privacy
