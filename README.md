# rsa-message-translator-gui

This project is a Python application with a simple graphical interface that helps demonstrate how RSA encryption works. It uses small numbers to make the process easier to understand. The program was created for a discrete mathematics course and is intended only for learning, not for actual secure communication.

## Cryptographic Setup

The application uses the following fixed RSA parameters:

- **Prime numbers:**
  - p = 3
  - q = 11
- **Modulus:**
  - n = p × q = 33
- **Euler’s totient:**
  - φ(n) = 20

### Public Key
- The public exponent **e** is selected from a dropdown of valid values such that  
  gcd(e, φ(n)) = 1

### Private Key
- The private exponent **d** is computed automatically using the modular inverse:
  - e × d ≡ 1 (mod 20)

## Encoding Scheme

Messages are encoded using the following numeric representation:

- **Letters:**
  - A = 01, B = 02, …, Z = 26
- **Space:**
  - 32
- **Punctuation:**
  - 27 = .
  - 28 = ,
  - 29 = ?
  - 30 = !
  - 31 = '

Uppercase and lowercase letters are treated as the same.
