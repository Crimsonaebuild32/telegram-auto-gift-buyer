# 🔒 Security Policy

## Reporting Security Vulnerabilities

We take security seriously. If you discover a security vulnerability, please report it responsibly.

### How to Report

**DO NOT** create a public GitHub issue for security vulnerabilities.

Instead:

1. **Email:** security@example.com
2. **Subject:** "Security Vulnerability - Telegram Auto Gift Buyer"
3. **Include:**
   - Description of the vulnerability
   - Steps to reproduce
   - Potential impact
   - Suggested fix (if any)

### Response Timeline

- **Initial Response:** Within 24 hours
- **Assessment:** Within 72 hours
- **Fix Release:** Depends on severity (1-14 days)
- **Public Disclosure:** After fix is deployed

### Security Hall of Fame

We recognize security researchers who responsibly disclose vulnerabilities.

---

## Supported Versions

| Version | Supported          |
| ------- | ------------------ |
| 2.0.x   | ✅ Yes            |
| 1.5.x   | ✅ Yes            |
| 1.4.x   | ⚠️ Security fixes only |
| < 1.4   | ❌ No             |

---

## Security Best Practices

### For Users

- ✅ Download only from official sources
- ✅ Enable two-factor authentication
- ✅ Use strong master password
- ✅ Keep software updated
- ✅ Review permissions carefully
- ✅ Use antivirus software

### For Developers

- ✅ Follow secure coding practices
- ✅ Validate all inputs
- ✅ Use parameterized queries
- ✅ Implement proper authentication
- ✅ Encrypt sensitive data
- ✅ Keep dependencies updated

---

## Known Security Considerations

### Data Storage

- All sensitive data is encrypted at rest (AES-256)
- Session tokens are stored securely
- Passwords are hashed (Argon2id)
- No plaintext credentials

### Network Communication

- TLS 1.3 for all connections
- Certificate pinning enabled
- No unencrypted transmissions
- Proxy support with authentication

### Authentication

- OAuth 2.0 with Telegram
- Two-factor authentication supported
- Session timeout after inactivity
- Secure session management

---

## Security Update Policy

- **Critical:** Immediate release
- **High:** Within 7 days
- **Medium:** Next regular release
- **Low:** Scheduled maintenance

---

**Last Updated:** June 11, 2026  
**Contact:** security@example.com
