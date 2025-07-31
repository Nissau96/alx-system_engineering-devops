# alx-system_engineering-devops

This directory contains scripts related to Shell initialization files, shell variables, expansions, and aliasing, tested on Ubuntu 20.04 LTS.

---

## 📄 Script Descriptions

### 0-alias
- **Purpose:** Creates an alias `ls` that will run `rm *`
- **Usage:**
  ```bash
  source ./0-alias
  ls     # This will now delete all files in the current directory!