# Linux Shell & Environments — Study Notes

## 1. What is a Shell?
* **Analogy:** A shell acts like a **container** (or Tupperware) within the operating system that holds the user's environment, variables, and session information.
* **Core Role:** An interface layer that sits between the **user / applications** and the **kernel**.
* **Primary Function:** Provides a platform or environment to input, interpret, and execute system commands.

---

## 2. Types of Shell Interfaces

| Type | Description | Examples |
| :--- | :--- | :--- |
| **GUI Shell (Graphical)** | Graphical interface where commands are executed via visual clicks and window interactions. | Windows GUI Explorer, Linux KDE Plasma, GNOME |
| **CLI Shell (Command-Line)** | Text-based prompt/terminal environment where commands are typed and executed directly. | `bash`, `sh`, `csh`, `zsh` |

---

## 3. Position in System Architecture

```
[ User / Applications ]
           |
           v
      [ SHELL ]  <-- (GUI or CLI: Translates user commands)
           |
           v
     [ KERNEL ]  <-- (Translates commands to system hardware)
           |
           v
    [ HARDWARE ]
```

---

## 4. Useful Linux Shell Commands & Inspection

* **Identify Active Shell:**
  ```bash
  echo $0
  ```
  *Prints the name of the currently running shell (e.g., `bash`).*

* **List All Available Shells on the System:**
  ```bash
  cat /etc/shells
  ```
  *Displays all installed and valid login shells available in the Linux distribution.*

* **Check a User's Assigned Default Shell:**
  ```bash
  cat /etc/passwd
  ```
  *Each entry in `/etc/passwd` specifies the user's default login shell at the very end of the line (e.g., `/bin/bash`).*

---

## 5. Key Takeaways
* Shells encapsulate the execution environment and can be customized or scripted to automate tasks.
* A user's assigned default shell can be reconfigured or changed if necessary.
* Whether using a mouse in a GUI or entering commands in a CLI, interactions are mediated by a shell before reaching the kernel.
