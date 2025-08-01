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
- **Command used:** `echo "hello $(whoami)"`
- **Usage:**
  ```bash
  ./1-hello_you
  # Output:
  hello julien

### 2-path
- **Purpose:** Adds `/action` to the end of the `PATH` environment variable.
- **Command used:** `export PATH="$PATH:/action"`
- **Usage:**
  ```bash
  source ./2-path
  echo $PATH
  # Output will include /action at the end

### 3-paths
- **Purpose:** Counts the number of **non-empty directories** listed in the `PATH` environment variable.
- **Command used:** `echo $PATH | tr ':' '\n' | wc -l`
- **Usage:**
  ```bash
  . ./3-paths
  # Output: 11 (or depending on your PATH)