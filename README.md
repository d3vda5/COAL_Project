# RSA Encryption and Decryption in MASM

This project implements RSA encryption and decryption using MASM (Microsoft Macro Assembler) with Irvine32 library support. The program allows users to encrypt a message and decrypt an encrypted message using the RSA algorithm.

## Features

- Generate random prime numbers for RSA key generation.
- Compute RSA public and private keys.
- Encrypt a message using the RSA public key.
- Decrypt an encrypted message using the RSA private key.
- Display the encrypted message in hexadecimal format.

## Prerequisites

- Microsoft Visual Studio with MASM support.
- Irvine32 library.

## Getting Started

1. **Clone the repository:**
```plaintext
  git clone https://github.com/d3vda5/COAL_Project.git
  cd COAL_Project
```

2. **Open the project in Visual Studio:**

    Open the `.sln` file in Visual Studio.

3. **Build the project:**

    Build the project using Visual Studio to compile the assembly code.

4. **Run the executable:**

    Run the generated executable to start the RSA encryption and decryption program.

## Usage

1. **Start the program:**

    When you run the program, you will be prompted with a menu:
```plaintext
    1) Start new encryption
    2) Decrypt a message
    Enter integer:
```

2. **Encrypt a message:**

    - Choose option `1` to start a new encryption.
    - Enter the message you want to encrypt (max 80 characters).
    - The program will generate RSA keys and display the encrypted message in hexadecimal format along with the RSA parameters (N, e, d).

3. **Decrypt a message:**

    - Choose option `2` to decrypt a message.
    - Enter the RSA parameters (N, d) and the encrypted message in hexadecimal format.
    - The program will decrypt the message and display the original message.

## Code Overview

- **Prime Number Generation:**
    - `getPrimeNumber`: Generates a random prime number within a specified range.
    - `isqrt`: Computes the integer square root of a number.

- **GCD and Inverse Calculation:**
    - `gcd`: Computes the greatest common divisor of two numbers.
    - `fullGcd`: Computes the extended GCD and the multiplicative inverse.
    - `inverse`: Computes the multiplicative inverse using the extended GCD.

- **Modular Exponentiation:**
    - `modPower`: Computes the modular exponentiation (base^exponent % modulus).

- **Main Procedure:**
    - `main`: Handles the user interface, encryption, and decryption processes.

## Example

Here is an example of encrypting and decrypting a message:

1. **Encrypt a message:**

```plaintext
  1) Start new encryption
  2) Decrypt a message
  Enter integer: 1
  Enter message to encrypt(max 80 characters): hello
  
  N= +218731277
  e= +189969083
  d= +80462387
  Remember these values for N, e, and d. You may need them for decryption
  Below is your encrypted message

  Dump of offset 008C62E2
  -------------------------------
  036C96BA  05402FF1  0CD90051  007F52A7  00000000  00000000  00000000  00000000  00000000  00000000  00000000  00000000  00000000    00000000  00000000  00000000  00000000  00000000  00000000  00000000  00000000  00000000  00000000  00000000  00000000  00000000  00000000  00000000  00000000  00000000  00000000  00000000  00000000  00000000  00000000  00000000  00000000  00000000  00000000  00000000
```

2. **Decrypt a message:**
```plaintext
  1) Start new encryption
  2) Decrypt a message
  Enter integer: 2

  N= 218731277

  d= 80462387

  Hex String= 036C96BA  05402FF1  0CD90051  007F52A7
  hello
```

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE.txt) file for details.

## Acknowledgments

- Irvine32 library for providing useful assembly routines.
- Microsoft Visual Studio for the development environment.
