# Decrypting Encrypted Files in Linux

## Scenario Overview

As a security analyst, you are tasked with decrypting encrypted files in your Linux home directory using basic cryptographic techniques, including the Caesar cipher and OpenSSL.

---

## Task 1: Read the Contents of a File

**Starting point:** `/home/analyst`

1. **List directory contents:**

   ```bash
   ls /home/analyst
   ```

   **Output:**
   ```
   Q1.encrypted
   README.txt
   caesar
   ```

2. **Read the README.txt file:**

   ```bash
   cat README.txt
   ```

   **Output:**
   ```
   Hello,
   All of your data has been encrypted. To recover your data, you will need to solve a cipher. To get started look for a hidden file in the caesar subdirectory.
   ```

**Summary:** Instructions direct you to locate a hidden file in the `caesar` subdirectory.

---

## Task 2: Find a Hidden File

1. **Navigate to the caesar subdirectory:**

   ```bash
   cd caesar
   ```

2. **List all files, including hidden ones:**

   ```bash
   ls -a
   ```

   **Output:**
   ```
   .
   ..
   .leftShift3
   ```

3. **Read the hidden file `.leftShift3`:**

   ```bash
   cat .leftShift3
   ```

   *(The contents appear scrambled using a Caesar cipher with a left shift of 3.)*

4. **Decrypt the Caesar cipher using `tr`:**

   ```bash
   cat .leftShift3 | tr "d-za-cD-ZA-C" "a-zA-Z"
   ```

   **Output:**
   ```
   In order to recover your files you will need to enter the following command:

   openssl aes-256-cbc -pbkdf2 -a -d -in Q1.encrypted -out Q1.recovered -k ettubrute
   ```

5. **Return to the home directory:**

   ```bash
   cd ~
   ```

---

## Task 3: Decrypt the File

1. **Use the `openssl` command to decrypt the encrypted file:**

   ```bash
   openssl aes-256-cbc -pbkdf2 -a -d -in Q1.encrypted -out Q1.recovered -k ettubrute
   ```

   **Command breakdown:**
   - `openssl`: cryptography tool
   - `aes-256-cbc`: encryption algorithm
   - `-pbkdf2`: strengthens the password using key derivation
   - `-a`: base64 encoding
   - `-d`: decrypt mode
   - `-in`: input file
   - `-out`: output file
   - `-k`: key/password (`ettubrute`)

2. **Confirm the decrypted file exists:**

   ```bash
   ls
   ```

   **Output includes:**
   ```
   Q1.recovered
   ```

3. **Read the decrypted file:**

   ```bash
   cat Q1.recovered
   ```

   *(This typically reveals the final message confirming successful decryption.)*

---

## Conclusion

You’ve successfully practiced the following skills using Linux Bash commands:

- Listing hidden files
- Decrypting a Caesar cipher
- Decrypting files with OpenSSL
