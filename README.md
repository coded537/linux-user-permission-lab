# linux-user-permission-lab
# Linux User and Group Permission Lab

## Project Overview

This project demonstrates how Linux users, groups, and file permissions can be used to control access to company resources. The lab simulates a company with different departments where each employee can only access their own department's folder.

---

## Goal of the Lab

The goal of this project was to learn how Linux access control works by:

- Creating users and groups.
- Assigning users to the correct groups.
- Creating department directories.
- Setting directory permissions.
- Testing that unauthorized users receive "Permission denied."

---

## Users and Groups Created

### Users

- Alice
- Bob
- Charlie

### Groups

- developers
- security
- HR

Each user was added to the appropriate department group.

| User | Group |
|-------|--------|
| Alice | developers |
| Bob | security |
| Charlie | HR |

---

## Permissions Configuration

The following Linux commands were used:

- adduser
- groupadd
- usermod -aG
- chgrp
- chmod
- su
- id
- groups

Group ownership was changed so that each department folder belonged to its respective group.

Permissions were configured using symbolic chmod commands such as:

```bash
chmod o-r Developers
chmod o-x Developers
```

This removed access from users outside the assigned group.

---

## Testing Access

The project was tested by switching between users using:

```bash
su alice
su bob
su charlie
```

Each user attempted to access every department folder.

Results:

- Alice could access Developers only.
- Bob could access security only.
- Charlie could access HR only.
- Unauthorized access resulted in:

```
Permission denied
```

This confirmed that the permissions were working correctly.

---

## What I Learned

From this project I learned:

- The difference between Linux users and groups.
- How to create users and groups.
- How to assign users to groups.
- How Linux permissions (rwx) work.
- How to use chmod with symbolic notation.
- The difference between "Permission denied" and "Command not found."
- That parent directory permissions affect access to subdirectories.
- The importance of least privilege in securing Linux systems.

---

## Skills Demonstrated

- Linux Administration
- User Management
- Group Management
- File Permissions
- Access Control
- Command Line
- Cybersecurity Fundamentals

---

## Author

Oshomah Silas
