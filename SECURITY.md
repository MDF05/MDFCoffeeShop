# Security Policy

## Supported Versions

Use this section to tell people about which versions of your project are currently being supported with security updates.

| Version | Supported          |
| ------- | ------------------ |
| 1.0.x   | :white_check_mark: |
| < 1.0   | :x:                |

## Reporting a Vulnerability

We take the security of our software seriously. If you have discovered a security vulnerability, we appreciate your help in disclosing it to us in a responsible manner.

### Process

1.  **Do not create a public issue** on GitHub for security vulnerabilities.
2.  Send an email to **[INSERT EMAIL HERE]** with a detailed description of the vulnerability.
3.  Include steps to reproduce the issue, if possible.
4.  Our security team will review your report and respond within 48 hours.
5.  We will work with you to understand and resolve the issue.

### Timeline

*   **Acknowledgement**: Within 48 hours.
*   **Assessment**: Within 5 business days.
*   **Fix**: Timeline depends on severity, but we aim for < 14 days for critical issues.

### Disclosure

We request that you do not publicly disclose the vulnerability until we have had reasonable time to address it. We will coordinate the public disclosure with you.

## Security Best Practices for Developers

- Ensure all dependencies are up to date (`npm audit`).
- Do not commit secrets (API keys, passwords) to the repository.
- Use secure storage (e.g., `SecureStore` in Expo) for sensitive user data.
- Validate all user inputs on both client and server sides.
