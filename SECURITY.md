# Security Policy

## Supported Versions

| Version | Supported          |
| ------- | ------------------ |
| 1.x     | :white_check_mark: |

## Reporting a Vulnerability

If you discover a security vulnerability, please report it responsibly:

1. **Do NOT** create a public GitHub issue
2. Contact the maintainer directly through GitHub
3. Provide detailed information about the vulnerability
4. Allow reasonable time for a fix before public disclosure

## Security Features

Tactic Remote includes several security features:

- **API Key Authentication** - Optional authentication for server access
- **Path Restrictions** - File operations limited to allowed directories
- **Input Validation** - All inputs are validated and sanitized
- **Rate Limiting** - Protection against brute-force attacks

## Best Practices

When using Tactic Remote:

1. **Use API Key** - Enable authentication in production
2. **Restrict Paths** - Limit file access to project directories only
3. **Use Cloudflare Tunnel** - For secure public access with TLS
4. **Keep Updated** - Always use the latest version
