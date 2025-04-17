# Scenario

You are a security professional at a large organization working primarily with the research team. One of your responsibilities is to ensure users have the correct permissions to access files and directories—ensuring that only authorized users have access.

Your task involves:

- Examining existing file system permissions  
- Determining if permissions align with required access  
- Modifying permissions if needed to restrict or grant access  

This scenario aligns with the *Manage Authorization* lab. You may revisit the lab to capture screenshots for your portfolio or use the provided command templates.

As part of this task, you will create a portfolio document to demonstrate your ability to use Linux commands to manage file permissions. This document can be added to your cybersecurity portfolio, which may be shared with potential employers or recruiters. Your goal is to explain and showcase the commands you used, helping you prepare for job interviews and other hiring processes.

---

# File Permissions in Linux

## Project Description

In this project, I demonstrated how to examine and manage file and directory permissions in Linux using common terminal commands. The objective was to ensure only authorized users had appropriate access levels, aligning with security best practices. This scenario simulated a real-world task where permissions needed to be reviewed and modified to protect sensitive research data.

## Check File and Directory Details

To check permissions of all files in a directory, including hidden files, I used the following command:

```bash
ls -la /home/researcher2/projects
```

This command displays detailed file information, including ownership and the 10-character permission string for each file and directory. Based on the *Current file permissions* document, the output can be represented with the following permission strings:

```plaintext
project_k.txt:    -rw-rw-rw-
project_m.txt:    -rw-r-----
project_r.txt:    -rw-rw-r--
project_t.txt:    -rw-rw-r--
.project_x.txt:   -rw--w----
drafts/:          drwx--x---
```

## Describe the Permissions String

Example: `-rw-rw-r--`

- The first character `-` indicates this is a regular file (not a directory).
- The next three characters `rw-` represent the user (owner) permissions: read and write.
- The middle three `rw-` represent the group permissions: read and write.
- The last three `r--` represent the other (everyone else) permissions: read only.

This permission string shows that the user and group can read and write to the file, while others can only read it.

## Change File Permissions

The organization’s policy does not allow other users to have write access.  
From the list, `project_k.txt` has `other = write`, which violates this rule.  
To remove write access for others, I used this command:

```bash
chmod o-w /home/researcher2/projects/project_k.txt
```

Resulting permission string:

```plaintext
-rw-rw-r--
```

This ensures that only the user and group can write to the file, while others can still read it.

## Change File Permissions on a Hidden File

The file `.project_x.txt` is hidden and archived. It should have:

- User: read only
- Group: read only
- Other: no access

To assign these permissions, I used the following standard symbolic format:

```bash
chmod u=r,g=r,o= /home/researcher2/projects/.project_x.txt
```

This command sets user (u) and group (g) to read-only and removes all permissions for others (o=).

As an alternative advanced option, I could also use the octal representation:

```bash
chmod 440 /home/researcher2/projects/.project_x.txt
```

Here, `4` represents read permission (`r`), and `0` indicates no permissions. The digits correspond to user, group, and other respectively:

- `4` (user): read
- `4` (group): read
- `0` (other): none

## Change Directory Permissions

The `drafts/` directory should only be accessible by the `researcher2` user. Group and other users should have no access.  
To set this, I used the symbolic format:

```bash
chmod u=rwx,g=,o= /home/researcher2/projects/drafts
```

This grants the user full access (read, write, execute), and removes all permissions from group and others.

As an alternative advanced option, the same can be achieved using the octal format:

```bash
chmod 700 /home/researcher2/projects/drafts
```

The octal value `7` means full permissions (`rwx`), and `0` removes all permissions. This applies to:

- `7` (user): read, write, execute
- `0` (group): none
- `0` (other): none

## Summary

In this activity, I reviewed and modified file and directory permissions using Linux commands. I checked current permissions using `ls -la`, interpreted permission strings, and used `chmod` to correct security issues. These changes ensured that unauthorized users no longer had access to sensitive research files. This task reflects real-world responsibilities in maintaining system security and enforcing proper authorization policies.
