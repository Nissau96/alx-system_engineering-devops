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

<details>
<summary><strong>11. There are 10 types of people in the world -- Those who understand binary, and those who don't</strong></summary>

Write a script that converts a number from base 2 to base 10.

- The number in base 2 is stored in the environment variable `BINARY`
- The script should display the number in base 10, followed by a new line
- **File:** `11-binary_to_decimal`

<details>
<summary>Example:</summary>

```bash
$ export BINARY=10100111001
$ ./11-binary_to_decimal
1337
</details> </details> 

```

<details>
<summary><strong>12. Combination</strong></summary>

Create a script that prints all possible combinations of two lowercase letters, from `a` to `z`, except `oo`.

- One combination per line
- The output is ordered alphabetically starting from `aa`
- Do not print `oo`
- The script must contain **a maximum of 64 characters**

**File:** `12-combinations`

<details>
<summary>Example:</summary>

```bash
$ ./12-combinations | wc -l
675

$ ./12-combinations | grep oo
# (no output)

$ ./12-combinations | tail -303 | head -10
oi
oj
ok
ol
om
on
op
oq
or
os
</details> </details> 
```

<details>
<summary><strong>13. Floats</strong></summary>

Write a script that prints a number with **two decimal places**, followed by a new line.

- The number is stored in the environment variable `NUM`.
- The output should **always show two digits after the decimal**.

**File:** `13-print_float`

<details>
<summary>Example:</summary>

```bash
$ export NUM=0
$ ./13-print_float
0.00

$ export NUM=98
$ ./13-print_float
98.00

$ export NUM=3.14159265359
$ ./13-print_float
3.14
</details> </details> 
```

### 14. Decimal to Hexadecimal

**File:** `100-decimal_to_hexadecimal`

A Bash script that converts a number from base 10 to base 16.

- The decimal number is stored in the environment variable `DECIMAL`.
- The script prints the hexadecimal representation of the number, followed by a new line.

#### Example:

```bash
export DECIMAL=1337
./100-decimal_to_hexadecimal
# Output: 539
```

### 15. Everyone is a proponent of strong encryption

**File:** `101-rot13`

A Bash script that encodes and decodes text using the ROT13 encryption technique.

- Assumes input text is ASCII.
- The script reads from standard input and outputs ROT13-encoded text.
- ROT13 is symmetric, so encoding the output again decodes it.

#### Example:

Given a file named `quote` with the content:
```text
"Everyone is a proponent of strong encryption."

- Dorothy E. Denning

```
### 16. The eggs of the brood need to be an odd number

**File:** `102-odd`

A Bash script that prints every other line from standard input, starting with the first line.

- Uses `awk` to filter and output only odd-numbered lines.
- Accepts piped input or reads directly from standard input.

#### Example Usage:

```bash
ls -1 | ./102-odd

Given:

bin
boot
dev
etc
home
...

Output:

dev
home
lib
lib64
lost+found
mnt
proc
run
srv
t
t~
usr
vmlinuz
```
