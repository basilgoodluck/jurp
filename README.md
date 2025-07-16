jurp
jurp is a Rust-based CLI tool for generating cryptographic secrets, keys, and development-safe identifiers. It's designed for developers who need secure values quickly from the terminal during setup, deployment, or local development.

Features
1. Cryptographic Secrets
Secure values used in authentication, token signing, and password generation.

jwt-secret – Generate HMAC-safe random secrets for JWTs.

password – Generate strong, random passwords.

rsa-key – Generate RSA key pairs (private + public PEM).

2. Identifiers
Unique values used in APIs, resources, and system references.

uuid – Generate a UUID v4.

(Planned: ulid, snowflake)

3. Encoders
Basic string encoding tools commonly used in dev workflows.

base64 – Encode strings to base64.

Installation
bash
Copy
Edit
cargo install --git https://github.com/yourusername/jurp
Requires Rust installed.

Usage
bash
Copy
Edit
jurp generate <command> [options]
Commands
Command	Description
jwt-secret	Generate a secure JWT secret string
password	Generate a strong random password
rsa-key	Generate RSA key pair (PEM format)
uuid	Generate a UUID v4
base64	Encode a string to base64

Examples
bash
Copy
Edit
jurp generate jwt-secret
jurp generate password --length 24
jurp generate rsa-key
jurp generate uuid
jurp generate base64 --data "hello world"
Planned Features
--output: Write generated values to files or .env

--copy: Copy results to clipboard

--file: Base64-encode contents of a file

ulid, bcrypt, argon2, and QR output

Contributing
Pull requests are welcome. New generators, output formats, or improvements are encouraged.

License
MIT License — see LICENSE file for details.
