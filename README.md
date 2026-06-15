# Secure-Message-Transmission-RSA
Secure Message Transmission Using RSA-2048 Asymmetric Encryption and OpenSSL

## Overview
This project demonstrates secure message transmission using RSA-2048 asymmetric encryption with OpenSSL. A message is encrypted using the receiver's public key and decrypted using the corresponding private key.

## Objectives

Understand asymmetric encryption
Generate RSA public and private keys
Encrypt a message using a public key
Decrypt a message using a private key
Demonstrate secure communication

## Tools Used
OpenSSL
RSA-2048
Linux/Windows

## Steps

## Generate Private Key
bash
openssl genrsa -out private.pem 2048

## Generate Public Key
bash
openssl rsa -in private.pem -pubout -out public.pem

## Create Message
bash
echo "Confidential Company Information" > message.txt

## Encrypt Message
bash
openssl pkeyutl -encrypt -pubin -inkey public.pem -in message.txt -out encrypted.bin

## Decrypt Message
bash
openssl pkeyutl -decrypt -inkey private.pem -in encrypted.bin -out decrypted.txt

## Verify Output
bash
cat decrypted.txt

## Output:
text
Confidential Company Information

## Results

-RSA key pair generated successfully
-Message encrypted successfully
-Secure transmission achieved
-Original message recovered using the private key

## Applications
-Secure Email Communication
-SSL/TLS Certificates
-Digital Signatures
-Online Banking
-Secure File Transfer

## Conclusion

This project demonstrates how RSA-2048 asymmetric encryption can be used to securely transmit confidential information over an untrusted network using OpenSSL.



## ⭐ If you found this project useful, please consider giving it a Star!
