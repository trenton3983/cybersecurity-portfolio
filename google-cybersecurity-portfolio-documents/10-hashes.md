# Activity Overview

As a security analyst, it's essential to implement controls that verify file integrity and detect tampering. One way to do this is by generating and comparing **hash values** using a **hash function**—an algorithm that produces a fixed-length code known as a **digest** or **hash value**.

Hash functions are commonly used to:

- Detect whether files have been modified.
- Verify authenticity between original and suspicious files.
- Identify malicious code by detecting even minor file changes.

This lab guides you through generating and comparing hashes manually using Linux commands.

---

# Scenario

You’ve been tasked with verifying whether two files, `file1.txt` and `file2.txt`, are truly identical, despite appearing the same on visual inspection.

You will:

1. Display file contents  
2. Generate hashes using `sha256sum`  
3. Compare the hash values manually and programmatically  

---

# Task 1: Generate Hashes for Files

You're in the default working directory `/home/analyst`, which contains two files: `file1.txt` and `file2.txt`.

## Step 1: List directory contents

**Command:**

```bash
ls
```

**Expected output:**

```
file1.txt file2.txt
```

## Step 2: Display the contents of both files

**Commands:**

```bash
cat file1.txt
cat file2.txt
```

**Expected output for both:**

```
X5O!P%@AP[4\PZX54(P^)7CC)7}$EICAR-STANDARD-ANTIVIRUS-TEST-FILE!$H+H*
```

**Observation:** The files appear identical when viewed with `cat`.

## Step 3: Generate hash values

**Commands:**

```bash
sha256sum file1.txt
sha256sum file2.txt
```

**Expected output:**

- `file1.txt` hash:
  ```
  131f95c51cc819465fa1797f6ccacf9d494aaaff46fa3eac73ae63ffbdfd8267
  ```

- `file2.txt` hash:
  ```
  2558ba9a4cad1e69804ce03aa2a029526179a91a5e38cb723320e83af9ca017b
  ```

**Conclusion:** Although the content appears the same, the **hashes differ**, which indicates a difference at the data level.

---

# Task 2: Compare Hashes

## Step 1: Write each file’s hash to a new file

**Commands:**

```bash
sha256sum file1.txt >> file1hash
sha256sum file2.txt >> file2hash
```

## Step 2: View hash files

**Commands:**

```bash
cat file1hash
cat file2hash
```

**Note:** You will see the same differing hash values stored in separate files.

## Step 3: Use the `cmp` command to compare the hash files

**Command:**

```bash
cmp file1hash file2hash
```

**Expected output:**

```
file1hash file2hash differ: char 1, line 1
```

**Conclusion:** The `cmp` command confirms the hashes differ at the **first character**, meaning the underlying content is not identical.

---

# Conclusion

You’ve successfully learned how to:

- Generate hashes using `sha256sum`
- Display hash values using `cat`
- Compare hash outputs using `cmp`

These Linux tools are crucial for validating **data integrity** and identifying **malicious file changes**, helping security analysts detect tampering or substitution of files, even when changes aren't visible.
