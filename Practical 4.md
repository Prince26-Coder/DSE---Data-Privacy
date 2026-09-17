
# Cryptography

## 1. Introduction

Cryptography is the practice of protecting information by transforming it into a secure form so that only authorized users can access or verify it.

In this project, students will learn about different cryptographic techniques, including encryption, hashing, and digital signatures. Students will also implement these techniques using appropriate programming languages and cryptographic libraries.

## 2. Objectives

The main objectives of this project are:

- Understand the basic concepts of cryptography.
- Learn the difference between symmetric and asymmetric cryptography.
- Understand encryption and decryption.
- Learn how cryptographic hashing works.
- Understand digital signatures and their purpose.
- Explore commonly used cryptographic algorithms.
- Use cryptographic libraries and tools.
- Implement basic cryptographic operations in practice.
- Understand the importance of secure key management.

## 3. Cryptographic Techniques

### 3.1 Encryption

Encryption converts readable information (plaintext) into an unreadable form (ciphertext).

```text
Plaintext
    |
    v
Encryption + Key
    |
    v
Ciphertext
    |
    v
Decryption + Key
    |
    v
Plaintext
````

 Encryption can be divided into two major categories:

 #### Symmetric Encryption

 Symmetric encryption uses the same secret key for encryption and decryption.

 Examples:

 - AES
- ChaCha20

 Basic process:

```
Plaintext + Secret Key
        |
        v
    Encryption
        |
        v
    Ciphertext
        |
        v
    Decryption
        |
        v
Plaintext
```

 #### Asymmetric Encryption

 Asymmetric encryption uses a pair of keys:

 - Public key
- Private key

 Examples:

 - RSA
- Elliptic Curve Cryptography (ECC)

 Basic process:

```
Message
   |
   v
Public Key
   |
   v
Encrypted Message
   |
   v
Private Key
   |
   v
Original Message
```

 ## 4\. Hashing

 Hashing converts input data into a fixed-length value called a hash or digest.

 Unlike encryption, hashing is designed to be one-way and does not normally provide a method to recover the original input from the hash.

 Examples:

 - SHA-256
- SHA-512
- SHA-3

 Example:

```
Input Data
    |
    v
Hash Function
    |
    v
Hash Value
```

 Hashing can be used for:

 - Data integrity verification
- File integrity checking
- Password protection when used with appropriate password-hashing algorithms
- Digital signatures
- Identifying changes to data

 > Note: General-purpose hashes such as SHA-256 should not be used alone for storing passwords. Passwords should be protected using dedicated password-hashing algorithms such as Argon2, scrypt, or bcrypt.

 ## 5\. Digital Signatures

 A digital signature is a cryptographic mechanism used to provide authenticity and integrity for digital data.

 Digital signatures typically use asymmetric cryptography.

 Basic process:

```
Message
   |
   v
Hash Function
   |
   v
Message Digest
   |
   v
Private Key
   |
   v
Digital Signature
```

 The recipient can use the sender's public key to verify the signature.

 Digital signatures can help provide:

 - Authentication
- Data integrity
- Proof that the signature corresponds to the holder of the private key

 Examples of technologies and algorithms include:

 - RSA signatures
- ECDSA
- Ed25519

 ## 6\. Cryptographic Algorithms

 | Technique | Examples | Primary Purpose |
| --- | --- | --- |
| Symmetric Encryption | AES, ChaCha20 | Protect data confidentiality |
| Asymmetric Cryptography | RSA, ECC | Key exchange, encryption, signatures |
| Hashing | SHA-256, SHA-3 | Integrity and data verification |
| Password Hashing | Argon2, scrypt, bcrypt | Secure password storage |
| Digital Signatures | RSA-PSS, ECDSA, Ed25519 | Authentication and integrity |

## 7\. Practical Implementation

 Students can implement cryptographic operations using a programming language such as Python.

 Recommended libraries include:

 - Python `cryptography` library
- OpenSSL
- Java Cryptography Architecture (JCA)
- Other established cryptographic libraries

 ### Example Project Structure

```
cryptography-project/
│
├── README.md
├── encryption/
│   ├── symmetric_encryption.py
│   └── asymmetric_encryption.py
│
├── hashing/
│   └── hash_demo.py
│
├── digital-signatures/
│   └── signature_demo.py
│
├── tests/
│   └── test_crypto.py
│
└── requirements.txt
```

 ## 8\. Suggested Practical Tasks

 ### Task 1: Symmetric Encryption

 Implement a program that:

 1. Accepts a sample message.
2. Generates or securely obtains a cryptographic key.
3. Encrypts the message.
4. Displays the ciphertext.
5. Decrypts the ciphertext.
6. Verifies that the original message has been recovered.

 ### Task 2: Hashing

 Create a program that:

 1. Accepts a text input or file.
2. Calculates its SHA-256 hash.
3. Displays the resulting hash.
4. Modifies the input.
5. Calculates the hash again.
6. Compares the two hash values.

 The goal is to demonstrate how even a small change in input produces a different hash.

 ### Task 3: Digital Signatures

 Create a program that:

 1. Generates a public/private key pair.
2. Creates a digital signature for a message.
3. Verifies the signature using the public key.
4. Modifies the message.
5. Attempts verification again.
6. Demonstrates that the modified message does not pass the original signature verification.

 ## 9\. Security Considerations

 When implementing cryptographic systems, students should consider:

 - Use well-established cryptographic algorithms.
- Do not create custom encryption algorithms for real-world security.
- Generate cryptographic keys using secure random number generators.
- Protect private keys from unauthorized access.
- Never hard-code production secrets or private keys in source code.
- Use secure key storage where appropriate.
- Use authenticated encryption, such as AES-GCM or ChaCha20-Poly1305, when confidentiality and integrity are both required.
- Use dedicated password-hashing algorithms for password storage.
- Keep cryptographic libraries updated.
- Avoid deprecated or insecure algorithms.

 ## 10\. Tools

 Students may use the following tools:

 | Tool | Purpose |
| --- | --- |
| Python | Cryptography implementation |
| OpenSSL | Encryption, hashing, certificates, and key management |
| `cryptography` | Python cryptographic library |
| Git | Version control |
| GitHub | Project hosting and documentation |

## 11\. Expected Deliverable

 The final project should contain:

 1. Introduction to cryptography
2. Explanation of symmetric encryption
3. Explanation of asymmetric cryptography
4. Explanation of hashing
5. Explanation of digital signatures
6. Comparison of cryptographic techniques
7. Practical implementations
8. Source code
9. Test cases
10. Screenshots or output examples
11. Security considerations
12. Conclusion
13. References

 ## 12\. Testing

 The implementation should be tested using different inputs.

 | Test Case | Input | Expected Result |
| --- | --- | --- |
| T01 | Normal text | Correct encryption and decryption |
| T02 | Empty input | Handled appropriately |
| T03 | Long text | Correct processing |
| T04 | Modified ciphertext | Verification/decryption should fail appropriately |
| T05 | Modified signed message | Digital signature verification should fail |
| T06 | Modified file | Hash value should change |

## 13\. Ethical Considerations

 Cryptography should be used responsibly.

 Students should:

 - Use cryptography for legitimate educational and security purposes.
- Protect private keys and sensitive information.
- Avoid publishing real passwords, private keys, or confidential data.
- Use test data during demonstrations.
- Avoid attempting to decrypt or access information without authorization.
- Clearly document the limitations of educational implementations.

 ## 14\. Conclusion

 Cryptography provides essential techniques for protecting information and establishing trust in digital systems.

 Through this project, students can gain practical experience with encryption, hashing, and digital signatures. Implementing these techniques helps students understand how cryptographic algorithms provide confidentiality, integrity, authentication, and other security properties.

 The project also demonstrates the importance of selecting appropriate algorithms, securely managing cryptographic keys, and using established cryptographic libraries instead of developing custom security mechanisms.

```

```
