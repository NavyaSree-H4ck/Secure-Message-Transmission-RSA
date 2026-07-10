# Secure Message Transmission Using RSA-2048 Asymmetric Encryption and OpenSSL

## Overview

This project demonstrates secure message transmission using RSA-2048 asymmetric encryption with OpenSSL. A message is encrypted using the receiver's public key and decrypted using the corresponding private key, ensuring confidentiality during transmission.

> **Disclaimer:** This project was conducted in a controlled laboratory environment for educational and cybersecurity learning purposes only.

## Objectives

- Understand asymmetric encryption.
- Generate RSA-2048 public and private keys.
- Encrypt a message using the receiver's public key.
- Decrypt the message using the corresponding private key.
- Demonstrate secure communication using OpenSSL.

## Lab Environment

| Component | Technology |
|-----------|------------|
| Operating System | Linux / Windows |
| Cryptography Tool | OpenSSL |
| Encryption Algorithm | RSA-2048 |
| Key Type | Public Key Infrastructure (PKI) |
| Files Used | private.pem, public.pem, message.txt |

## Repository Contents

- 📄 Project Report (PDF)
- 📝 Medium Walkthrough *(if available)*
- 📚 README Documentation

## Project Report

The complete project report, including commands, screenshots, observations, and encryption results, is available below.

📄 **Project Report:** [Secure_Message_Transmission_RSA_Report.pdf](Secure_Message_Transmission_RSA_Report.pdf)

## Procedure

### Step 1: Generate the RSA Private Key

```bash
openssl genrsa -out private.pem 2048
```

### Step 2: Generate the RSA Public Key

```bash
openssl rsa -in private.pem -pubout -out public.pem
```

### Step 3: Create the Message

```bash
echo "Confidential Company Information" > message.txt
```

### Step 4: Encrypt the Message

```bash
openssl pkeyutl -encrypt -pubin -inkey public.pem -in message.txt -out encrypted.bin
```

### Step 5: Decrypt the Message

```bash
openssl pkeyutl -decrypt -inkey private.pem -in encrypted.bin -out decrypted.txt
```

### Step 6: Verify the Output

```bash
cat decrypted.txt
```

## Output

```
Confidential Company Information
```

## Results

- RSA-2048 key pair generated successfully.
- Message encrypted using the public key.
- Encrypted message securely transmitted.
- Original message successfully recovered using the private key.

## Applications

- Secure Email Communication
- SSL/TLS Certificates
- Digital Signatures
- Online Banking
- Secure File Transfer
- Public Key Infrastructure (PKI)

## Key Learning Outcomes

- Asymmetric Cryptography
- RSA-2048 Encryption
- Public and Private Key Management
- OpenSSL Commands
- Secure Message Transmission
- Cryptographic Concepts

## Skills Demonstrated

- Cryptography
- OpenSSL
- Linux Command Line
- Information Security
- Secure Communication
- Cybersecurity Fundamentals

## Conclusion

This project demonstrates how RSA-2048 asymmetric encryption can securely protect confidential information during transmission. By using a public key for encryption and a private key for decryption, the project illustrates one of the fundamental principles of modern public key cryptography.

## Author

**Navya Sree**

Cybersecurity Student | SOC Analyst Aspirant

- GitHub: [NavyaSree-H4ck](https://github.com/NavyaSree-H4ck)
- Medium: [@knavyasree](https://medium.com/@knavyasree)
- LinkedIn: [Navya Sree](https://www.linkedin.com/in/navya-sree23/)

## Support

If you found this project useful, consider ⭐ starring this repository. Your support is appreciated!
