## jurp

jurp is a Rust-based CLI tool for generating cryptographic secrets, keys, and development-safe identifiers. It's designed for developers who need secure values quickly from the terminal during setup, deployment, or local development.

### Features

1. **Cryptographic Secrets, Secure values used in authentication, token signing, and password generation.**

- `jwt-secret` – Generate HMAC-safe random secrets for JWTs.
- `password` – Generate strong, random passwords.
- `rsa-key` – Generate RSA key pairs (private + public PEM).

2. **IdentifiersUnique values used in APIs, resources, and system references.**

- `uuid` – Generate a UUID v4.
(Planned: ulid, snowflake)

3. **EncodersBasic string encoding tools commonly used in dev workflows.**

- `base64` – Encode strings to base64.

### Installation
```bash
cargo install --git https://github.com/basilgoodluck/jurp
```

Requires Rust installed.

### Usage
```bash
jurp generate <command> [options]
```

### Commands

```markdown
| Command        | Description                            |
|----------------|----------------------------------------|
| jwt-secret     | Generate a secure JWT secret string    |
| password       | Generate a strong random password      |
| rsa-key        | Generate RSA key pair (PEM format)     |
| uuid           | Generate a UUID v4                     |
| base64         | Encode a string to base64              |
|                |                                        |
```

### Examples
```bash
- jurp generate jwt-secret
- jurp generate password --length 24
- jurp generate rsa-key
- jurp generate uuid
- jurp generate base64 --data "hello world"
```

### Planned Features

- --output: Write generated values to files or .env
- --copy: Copy results to clipboard
- --file: Base64-encode contents of a file
- ulid, bcrypt, argon2, and QR output

### Contributing
Contributions are currently closed, but feel free to clone the repo and explore or modify it as you like.

### License
MIT License — see [LICENSE file](https://github.com/basilgoodluck/jurp?tab=MIT-1-ov-file) for details.