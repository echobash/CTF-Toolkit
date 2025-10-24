# 🌐 CTF Web Security Tools & Resources

A comprehensive collection of web security tools, scripts, and resources for CTF competitions and penetration testing.

## 📋 Table of Contents

- [Online Web Resources](#-online-web-resources)
- [Reconnaissance Tools](#-reconnaissance-tools)
- [Exploitation Scripts](#-exploitation-scripts)
- [Analysis Tools](#-analysis-tools)
- [Bug Hunting Resources](#-bug-hunting-resources)
- [Hash & Crypto Tools](#-hash--crypto-tools)
- [MD5 Hash Collision Examples](#-md5-hash-collision-examples)
- [Usage Examples](#-usage-examples)

---

## 🌐 Online Web Resources

| Purpose | Resource Link |
|---------|---------------|
| Crack the Hashes from hashes stored in DB | [crackstation](https://crackstation.net/) |
| JWT Decoding etc. | [jwt.io](https://jwt.io) |
| JWK To PEM Convertor | [8gwifi](https://8gwifi.org/jwkconvertfunctions.jsp) |
| JWK Generator | [mkjwk](https://mkjwk.org/) |
| JS Deobfuscator | [Deobfuscate.io](https://deobfuscate.io/) |

---

## 🔍 Reconnaissance Tools

### GitHub Reconnaissance
- **File**: `Github Recon Words`
- **Purpose**: Comprehensive list of keywords and patterns for GitHub reconnaissance
- **Usage**: Use these patterns with GitHub search to find sensitive information, API keys, passwords, and secrets
- **Example**: Search for `API_KEY=` or `password=` in public repositories

### Google Dorks
- **File**: `Google Dorks For Finding RDP`
- **Purpose**: Google dorking queries to find RDP (Remote Desktop Protocol) services
- **Usage**: Use these queries in Google search to discover exposed RDP services
- **Example**: `intext:"we will work with you to resolve the issue promptly."`

---

## 💥 Exploitation Scripts

### URL Testing Script
- **File**: `requesturl.py`
- **Purpose**: Tests multiple URL combinations for availability
- **Usage**: 
  ```bash
  python3 requesturl.py
  ```
- **Description**: Checks if various URL combinations are accessible (currently configured for imgur.com)

### Robots.txt Downloader
- **File**: `robots.sh`
- **Purpose**: Downloads robots.txt file from CTFTime
- **Usage**:
  ```bash
  chmod +x robots.sh
  ./robots.sh
  ```
- **Description**: Downloads robots.txt to analyze disallowed directories and files

---

## 🔬 Analysis Tools

### Magic Hash Analysis
- **File**: `magicSha1`
- **Purpose**: Contains magic SHA1 hashes for hash collision attacks
- **Usage**: Use these hashes to bypass authentication systems vulnerable to hash collision attacks

### PHP Magic Hashes
- **File**: `phpMagicHashes`
- **Purpose**: Collection of magic hashes specific to PHP applications
- **Usage**: Useful for bypassing PHP-based authentication systems

---

## 🐛 Bug Hunting Resources

### Rate Limit Bypass
- **File**: `No Rate Limit Bug Finding`
- **Purpose**: Techniques for finding and exploiting rate limiting vulnerabilities
- **Usage**: Use these techniques to identify applications without proper rate limiting

### OTP Bypass Techniques
- **File**: `OTP Bypass`
- **Purpose**: Methods to bypass One-Time Password (OTP) systems
- **Usage**: Apply these techniques when testing OTP implementations

### Subscription Exploit
- **File**: `get free subscribers`
- **Purpose**: Exploit technique for manipulating subscriber counts
- **Usage**: 
  1. Subscribe to channel using username and capture the request
  2. Send it to intruder and remove auth_token param
  3. Start attack for desired number of subscribers
  4. Verify the subscriber count change

---

## 🔐 Hash & Crypto Tools

### Magic SHA1 Hashes
- **File**: `magicSha1`
- **Purpose**: Pre-computed SHA1 hashes that collide with common passwords
- **Usage**: Use these hashes to bypass authentication systems that use SHA1

---

## 🔐 MD5 Hash Collision Examples

### Magic MD5 Collision Strings
These two strings produce the same MD5 hash, demonstrating MD5 collision vulnerability:

```
String 1: TEXTCOLLBYfGiJUETHQ4hEcKSMd5zYpgqf1YRDhkmxHkhPWptrkoyz28wnI9V0aHeAuaKnak
String 2: TEXTCOLLBYfGiJUETHQ4hAcKSMd5zYpgqf1YRDhkmxHkhPWptrkoyz28wnI9V0aHeAuaKnak
```

**MD5 Hash**: Both strings produce the same MD5 hash value

### Usage
- Use these strings to test MD5 collision detection in applications
- Demonstrate MD5 vulnerability in CTF challenges
- Educational purposes for understanding hash collision attacks

### Security Implications
- MD5 is cryptographically broken and should not be used for security purposes
- These collisions can be exploited to bypass authentication systems
- Always use stronger hash functions like SHA-256 or SHA-3

---

## 💡 Usage Examples

### GitHub Reconnaissance Example
```bash
# Search for API keys in GitHub
site:github.com "API_KEY=" language:python

# Find configuration files with secrets
site:github.com "password=" extension:env

# Look for database credentials
site:github.com "mysql://" OR "postgresql://"
```

### Google Dorking Example
```bash
# Find exposed admin panels
site:target.com inurl:admin

# Find login pages
site:target.com inurl:login

# Find configuration files
site:target.com ext:conf OR ext:config
```

### Rate Limit Testing
```bash
# Test for rate limiting
for i in {1..100}; do
  curl -X POST "https://target.com/api/login" \
    -d "username=test&password=test" \
    -H "Content-Type: application/x-www-form-urlencoded"
done
```

---

## ⚠️ Legal Disclaimer

**IMPORTANT**: These tools are for educational purposes only. Only use them on systems you own or have explicit permission to test. Unauthorized access to computer systems is illegal and unethical.

## 🤝 Contributing

Found a new web security tool or technique? Feel free to contribute:

1. Add your tool/script to the appropriate category
2. Include clear usage instructions
3. Add examples where applicable
4. Update this README with your contribution

---

## 📚 Additional Resources

- [OWASP Web Security Testing Guide](https://owasp.org/www-project-web-security-testing-guide/)
- [PortSwigger Web Security Academy](https://portswigger.net/web-security)
- [HackerOne Hacker101](https://www.hacker101.com/)

---

<div align="center">
  <p><strong>Happy Hacking! 🚀</strong></p>
  <p>Remember: With great power comes great responsibility</p>
</div>