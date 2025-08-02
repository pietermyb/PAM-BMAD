# Security Best Practices

A condensed guide focusing on key principles across different domains.

## 1. General & Foundational

- **Secure by Design & Default:** Integrate security from the start of the SDLC. Configure systems to be secure out-of-the-box.
- **Principle of Least Privilege (PoLP):** Grant users, applications, and systems only the minimum permissions necessary.
- **Defense in Depth:** Implement multiple, overlapping security controls (technical and procedural).
- **Incident Response:** Develop, maintain, and test an incident response plan.
- **Security Awareness:** Train all personnel on security policies and threat identification (e.g., phishing).
- **Asset Management:** Keep all software, hardware, and third-party components patched and updated.

## 2. Application & Web Security

- **Input & Output Validation:** Treat all input as untrusted. Validate, sanitize, and encode all data to prevent Injection (SQLi, XSS) and SSRF.
- **Authentication & Session Management:** Enforce strong, multi-factor authentication (MFA). Securely manage session tokens (e.g., using HttpOnly cookies).
- **Access Control:** Implement and enforce robust, server-side access control (e.g., RBAC) to prevent broken access control vulnerabilities.
- **Secure Coding & Configuration:** Follow secure coding standards. Avoid hardcoded secrets. Use secure configurations for frameworks, servers, and headers (CSP, HSTS).
- **Dependency Management (SCA):** Use Software Composition Analysis (SCA) tools to find and remediate vulnerabilities in third-party libraries.
- **Continuous Testing (SAST/DAST):** Integrate Static and Dynamic Application Security Testing into the CI/CD pipeline.

## 3. Data Security

- **Data Classification:** Identify and classify data based on its sensitivity to apply appropriate controls.
- **Encryption:** Encrypt sensitive data at rest (e.g., in databases) and in transit (using TLS/HTTPS). Manage encryption keys securely.
- **Data Minimization & Disposal:** Collect only necessary data and securely delete it when no longer required.
- **Data Loss Prevention (DLP):** Use DLP tools to monitor and prevent unauthorized data exfiltration.
- **Backups:** Maintain and test secure, isolated backups.

## 4. Infrastructure & Network Security

- **System Hardening:** Reduce the attack surface by removing unnecessary services, ports, and software.
- **Network Segmentation:** Isolate critical systems by segmenting the network (e.g., using VLANs, firewalls).
- **Secure Configuration (IaC):** Use Infrastructure as Code (IaC) scanning to find misconfigurations in cloud environments.
- **Logging & Monitoring:** Aggregate logs and actively monitor for suspicious activity using tools like SIEM.
- **Secure Remote Access:** Enforce secure and authenticated remote access, typically via VPN or Zero Trust Network Access (ZTNA).