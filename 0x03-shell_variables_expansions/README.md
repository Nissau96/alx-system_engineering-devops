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
</details> </details> 
```

<details>
<summary><strong>9. Every addition to true knowledge is an addition to human power</strong></summary>

Write a script that prints the result of the addition of `128` with the value stored in the environment variable `TRUEKNOWLEDGE`, followed by a new line.

- **File:** `8-true_knowledge`

<details>
<summary>Example:</summary>

```bash
$ export TRUEKNOWLEDGE=1209
$ ./8-true_knowledge | cat -e
1337$
</details> </details> 
```

<details>
<summary><strong>9. Divide and rule</strong></summary>

Write a script that prints the result of `POWER` divided by `DIVIDE`, followed by a new line.

- **POWER** and **DIVIDE** are environment variables
- **File:** `9-divide_and_rule`

<details>
<summary>Example:</summary>

```bash
$ export POWER=42784
$ export DIVIDE=32
$ ./9-divide_and_rule
1337
</details> </details> 
```

<details>
<summary><strong>10. Love is anterior to life, posterior to death, initial of creation, and the exponent of breath</strong></summary>

Write a script that displays the result of `BREATH` to the power `LOVE`.

- **BREATH** and **LOVE** are environment variables
- The script should display the result followed by a new line
- **File:** `10-love_exponent_breath`

<details>
<summary>Example:</summary>

```bash
$ export BREATH=4
$ export LOVE=3
$ ./10-love_exponent_breath
64
</details> </details> 
```