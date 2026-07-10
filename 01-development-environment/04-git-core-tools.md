# Git and Core Development Tools

## Overview

A modern software development environment depends on several command-line tools that support version control, networking, downloading files, and archive management.

Within the Founder Builder Project, the primary tools are:

* Git
* Curl
* Wget
* Unzip

Rather than using the versions bundled with macOS, VTOBForge intentionally prioritizes the versions installed and managed through Homebrew.

This decision provides a more consistent, maintainable, and predictable development environment.

---

# Why These Tools Matter

Although Flutter is the primary application framework used in the Founder Builder Project, Flutter itself depends on many supporting tools.

For example:

* Git downloads Flutter updates and clones repositories.
* Curl securely communicates with web services.
* Wget downloads files from remote servers.
* Unzip extracts downloaded archives.

If these tools are outdated or behave differently across computers, development becomes more difficult to reproduce.

---

# Why Not Use the Built-in macOS Versions?

macOS includes its own versions of many development tools.

However, these versions are tied to the operating system and are not updated independently.

On older systems such as macOS Catalina, the bundled versions may:

* lack newer features,
* contain older bug fixes,
* differ from current open-source documentation,
* create compatibility issues with modern development workflows.

Using Homebrew allows these tools to be updated without upgrading the operating system.

---

# Prioritizing Homebrew Tools

The shell configuration gives priority to Homebrew-installed tools by adding their directories near the beginning of the PATH.

This means that when a command such as:

```bash
git
```

is executed, the shell uses the Homebrew version before checking the system version.

The same principle applies to Curl, Wget, and Unzip.

This produces a more consistent engineering environment across projects.

---

# Homebrew Environment Variables

The shell configuration contains the following settings:

```zsh
export HOMEBREW_FORCE_BREWED_GIT=1
export HOMEBREW_FORCE_BREWED_CURL=1
```

These variables instruct Homebrew to prefer its managed versions of Git and Curl whenever possible.

The objective is to reduce inconsistencies caused by older operating system tools.

---

# The brew-check Helper

The Founder Builder Project includes a helper command:

```bash
brew-check
```

This command reports:

* Git version and installation path.
* Curl version and installation path.
* Wget version and installation path.
* Unzip version and installation path.
* OpenSSL version and installation path.

Instead of checking every tool individually, one command provides a quick overview of the engineering environment.

This makes troubleshooting faster and helps verify that the intended Homebrew-managed tools are being used.

---

# Why Version Consistency Matters

Software engineering is more reliable when developers use consistent tool versions.

Different versions of the same tool can behave differently, leading to:

* unexpected errors,
* inconsistent builds,
* difficult debugging,
* documentation that no longer matches the installed software.

Managing these tools through Homebrew helps minimize these problems.

---

# Engineering Decision

The Founder Builder Project standardizes Homebrew-managed versions of Git, Curl, Wget, and Unzip.

Whenever practical, these versions are preferred over the copies bundled with the operating system.

This improves reproducibility, simplifies maintenance, and provides a more modern development experience.

---

# Lessons Learned

This stage reinforced several important engineering lessons.

**1. Development tools are part of the engineering system.**

Programming frameworks depend on a reliable collection of supporting utilities.

**2. Older operating systems should not prevent modern development.**

Using Homebrew allows modern tooling to run on older hardware while reducing dependence on outdated system utilities.

**3. Verification should be simple.**

A helper command such as `brew-check` makes it easy to confirm that the expected tools are installed and being used.

**4. Consistency reduces troubleshooting.**

When every project uses the same versions of essential tools, engineering becomes more predictable and easier to support.

---

# Future Direction

As additional command-line tools become part of the Founder Builder Project, they should follow the same principles:

* Install through a trusted package manager whenever appropriate.
* Document why the tool is required.
* Verify the installation.
* Keep the engineering environment consistent across projects.

The objective is not simply to accumulate tools but to maintain a development environment whose behavior is understood and reproducible.
