# alx-system_engineering-devops

This directory contains scripts related to Shell initialization files, shell variables, expansions, and aliasing, tested on Ubuntu 20.04 LTS.

---

## 📄 Script Descriptions

### 0-alias
- **Purpose:** Creates an alias `ls` that will run `rm *`
- **Usage:**
  ```bash
  source ./0-alias
  ls     

### 1-hello_you
- **Purpose:** Prints "hello <user>" where `<user>` is the current logged-in Linux user.
- **Command used:** `echo "hello $USER"`
- **Usage:**
  ```bash
  ./1-hello_you
  # Output:
  hello julien