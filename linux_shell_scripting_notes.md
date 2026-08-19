# Linux Shell Scripting — Study Notes

## 1. What is a Shell Script?
* **Definition:** An executable text file containing a series of shell commands designed to automate tasks [cite: 2, 4].
* **Execution Flow:** Commands inside a script run **sequentially** (top to bottom)—the first command executes, followed by the second, third, and so on [cite: 4].

---

## 2. Core Anatomy of a Shell Script

```bash
#!/bin/bash
# --------------------------------------------------
# Description: Example script showing core syntax
# --------------------------------------------------

# Commands & Logic
echo "Starting automation..."
mkdir -p /home/user/backup
```

### Component Breakdown
1. **The Shebang (`#!/bin/bash`):**
   * Placed on the **very first line** to specify which interpreter should execute the file [cite: 4].
   * `#` is called *pound/hash*, and `!` is called *bang* (together: **hashbang / shebang**) [cite: 4].
   * Points to the shell path (e.g., `#!/bin/bash` directs Linux to use the Bash shell) [cite: 4].
2. **Comments (`#`):**
   * Any line starting with a `#` (except the first shebang line) is treated as a comment [cite: 4].
   * Used to document script behavior, describe commands, or temporarily disable code [cite: 4].
3. **Commands:**
   * Standard Linux utilities, custom binaries, and built-in shell commands to be automated [cite: 4].
4. **Control Statements & Loops:**
   * Conditional logic (`if/then/else`) and iteration structures (`while`, `for`, `until`) that dictate workflow flow [cite: 4].

---

## 3. Permissions & Making Scripts Executable

* In Linux, a newly created script is treated as a standard flat text file without execute privileges by default [cite: 4].
* To run a script, it **must** have executable permissions (`x` bit) set for the user, group, or others [cite: 4].

```bash
# Add execute permission to the script
chmod +x my_script.sh
```

---

## 4. How to Execute a Shell Script

| Execution Method | Format | Example | Description |
| :--- | :--- | :--- | :--- |
| **Absolute Path** | `/full/path/to/script` | `/home/username/scripts/backup.sh` | Directly specifies the exact location from root (`/`) [cite: 4]. |
| **Relative Path (Current Dir)** | `./<script_name>` | `./backup.sh` | Uses `./` to tell the shell to look in the current working directory [cite: 4]. |

---

## 5. Summary Checklist
* [x] **Shebang:** Include `#!/bin/bash` on line 1 [cite: 4].
* [x] **Documentation:** Add comments starting with `#` [cite: 4].
* [x] **Permissions:** Enable execution with `chmod +x` [cite: 4].
* [x] **Execution:** Run via absolute path or relative path (`./script.sh`) [cite: 4].
