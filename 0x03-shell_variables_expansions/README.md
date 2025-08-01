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

### 4. Global variables

Create a script that lists environment variables.

- **File:** `4-global_variables`
- Must be exactly **2 lines**
- Must use the `printenv` command
- Must **not** use `&&`, `||`, `;`, `sed`, or `bc`

**Example:**
```bash
$ source ./4-global_variables
CC=gcc
CDPATH=.:~:/usr/local:/usr:/

```

## 5. Local variables

**Objective**:  
Create a script that lists all local variables, environment variables, and functions.

**File**: `5-local_variables`

### Requirements:
- Must be exactly **2 lines** long.
- Must use the `set` command.
- **Must not** use `&&`, `||`, `;`, `sed`, or `bc`.

---

### ✅ Example:

```bash
$ source ./5-local_variables
BASH=/bin/bash
BASHOPTS=checkwinsize:cmdhist:complete_fullquote:expand_aliases:...
# Output continues with all environment/local vars and shell functions
```

### 7. Local variable

Create a script that creates a new local variable.

- **Name:** `BEST`  
- **Value:** `School`  
- **File:** `6-create_local_variable`

#### Example:
```bash
$ source ./6-create_local_variable
$ echo $BEST
School
```

<details>
<summary><strong>8. Global variable</strong></summary>

Create a script that creates a new global variable.

- **Name:** `BEST`  
- **Value:** `School`  
- **File:** `7-create_global_variable`

<details>
<summary>Example:</summary>

```bash
$ source ./7-create_global_variable
$ echo $BEST
School
</details> </details> ```

