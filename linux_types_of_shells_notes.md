# Types of Linux Shells — Study Notes

## 1. Overview
A shell is an environment/interface for interacting with the operating system. In Linux, shells are broadly categorized into:
* **Graphical User Interface (GUI) Shells:** Visual desktop environments using mouse clicks and keyboard interactions.
* **Command-Line Interface (CLI) Shells:** Text-based terminal prompts for running commands and executing shell scripts.

---

## 2. GUI Desktop Shells

| Shell | Description | Interaction Style |
| :--- | :--- | :--- |
| **GNOME** | A widely used graphical desktop environment available during Linux installation. | Mouse clicks, drag-and-drop, windows, menus. |
| **KDE (KDE Plasma)** | A popular, customizable desktop graphical environment alternative. | Mouse clicks, desktop widgets, menus. |

---

## 3. Command-Line (CLI) Shells

### A. Bourne Shell (`sh`)
* **Creator:** Stephen Bourne at AT&T Bell Labs (1977).
* **Significance:** One of the original Unix/Linux shells; serves as the foundation for modern shells.
* **Key Features:**
  * I/O redirection (`<`, `>`).
  * Basic shell scripting (strings, integer variables, loops, conditional testing).
  * High compatibility across legacy Unix systems.

### B. Bourne-Again Shell (`bash`)
* **Definition:** An enhanced, backwards-compatible replacement for the original Bourne Shell (`sh`).
* **Adoption:** The standard default shell in most modern Linux distributions.
* **Key Features:**
  * Advanced scripting capabilities and rich variable handling.
  * Command history, tab-completion, and user-friendly interactive features.
  * Industry standard for general Linux administration and scripting.

### C. C Shell (`csh`) & TC Shell (`tcsh`)
* **`csh` (C Shell):**
  * **Creator:** Bill Joy at UC Berkeley (1977–1978).
  * **Syntax:** Modeled after the syntax of the C programming language.
* **`tcsh` (Enhanced C Shell):**
  * **Creator:** Ken Greer at Carnegie Mellon University.
  * **Features:** Enhanced interactive features (command-line editing, programmable word completion).
* **Important Note:** `csh` / `tcsh` scripts are **incompatible** with Bourne/Bash syntax. Generally recommended only for those specifically proficient in C/C++ or working in specialized legacy environments.

### D. KornShell (`ksh`)
* **Creator:** David Korn.
* **Compatibility:** Compatible with the Bourne Shell (`sh`) and shares many similarities with `bash`.
* **Key Features:**
  * Floating-point arithmetic.
  * Built-in job control and advanced programming constructs.
* **Common Use:** Heavily utilized in enterprise Unix environments (such as Oracle Solaris), whereas Linux environments predominantly default to `bash`.

---

## 4. Comparison Summary

| Shell | Executable | Creator | Key Characteristics | Common Environment |
| :--- | :--- | :--- | :--- | :--- |
| **Bourne** | `sh` | Stephen Bourne | Original standard, basic scripting | Legacy Unix / POSIX base |
| **Bourne-Again** | `bash` | Free Software Foundation | Enhanced `sh`, highly user-friendly | Default in most Linux distros |
| **C Shell** | `csh` | Bill Joy | C-language-like syntax | C developers, older BSD |
| **TC Shell** | `tcsh` | Ken Greer | Improved `csh` with CLI editing | Specialized C workflows |
| **KornShell** | `ksh` | David Korn | Fast, supports floating-point math | Enterprise Unix (Solaris) |

---

## 5. Checking & Managing Shells in Linux

* **List all installed shells:**
  ```bash
  cat /etc/shells
  ```
* **View user assigned shell:**
  ```bash
  cat /etc/passwd
  ```
* **Scripting Warning:** Always verify the target shell before writing scripts. A script written with Bash-specific syntax (Bashisms) may fail if executed in `csh`, `tcsh`, or pure `sh`.
