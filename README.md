# How Linux Works: An Upside-Down Tree

**Open the tutorial:** https://hossainms.github.io/how-linux-works/

An interactive, visual tutorial on how the Linux operating system is organized and what happens when you type a command. It is written for biomedical researchers and other scientists who run analyses on Linux workstations, high-performance computing (HPC) clusters and cloud systems.

## Overview

Most research computing today happens on Linux, yet many researchers learn it one command at a time without a picture of how the system fits together. This tutorial provides that picture through a single learning model, an upside-down tree:

| Part of the tree | Part of Linux | Examples |
|---|---|---|
| Roots | Hardware | CPU, memory, storage, network card, peripherals |
| Trunk | Kernel | scheduler, memory management, drivers, file systems, networking, security |
| Large branches | System components | system libraries (glibc), services (systemd, sshd), the shell (Bash) |
| Smaller branches | Tools | core utilities, file system tools, process tools, networking tools, package managers |
| Leaves | Applications | desktop apps, servers, development tools, data science tools, containers |
| Air and light | The outside world | users, networks, cloud platforms, other devices |

## Features

**The system view.** An animated diagram of every layer, from hardware to applications, with the system call interface marked between user space and kernel space. Select any part to see what it does, real examples, commands to try, and related files and interfaces. Four everyday tasks are animated step by step through the layers: typing `ls`, opening a website, plugging in a USB drive, and installing software with `apt`. Each animation plays automatically, one step at a time, and repeats until you press Pause; Previous and Next let you move at your own pace. The details panel follows each step, describing the part of the tree currently highlighted. Selecting any part yourself pauses the animation, so your selection stays on screen.

**The file system view.** The Linux directory hierarchy drawn as a tree growing from `/`, covering 18 top-level directories. A path locator shows where any path, such as `/usr/bin/python3` or `/etc/hostname`, sits in the hierarchy and what it is for.

**The story.** *A Day Inside the Tree* follows Safir, a research student in a genetics lab, through one working day at the terminal. Each chapter pairs a research task with a short command example, a plain-language explanation and a practical takeaway, and most can be played as an animation on the diagram.

| Time | Chapter | Topics |
|---|---|---|
| 08:30 | The tree wakes up | boot sequence, `/boot`, `/sbin`, systemd |
| 08:50 | How commands reach the system | system calls, user space and kernel space, `strace` |
| 08:55 | Two people, one computer | multi-user login, PAM, permissions, `sudo` |
| 09:10 | A home for the project | files and folders, page cache, `/home`, `/tmp` |
| 09:40 | Bash, the glue | pipelines, `PATH`, scripts, exit status |
| 10:15 | Growing a new leaf | installing software with APT, where software lives |
| 10:45 | A private toolbox | Python virtual environments |
| 11:30 | A terminal on another computer | SSH keys, `known_hosts`, `authorized_keys`, `scp`, `rsync` |
| 12:15 | Files that are not really files | `/proc`, `/dev`, system logs |
| 13:00 | Thousands of trees, one front door | HPC clusters, login and compute nodes, Slurm jobs |
| 14:30 | Docker and Apptainer: a tree in a box | containers, namespaces, cgroups, GPU access |
| 16:00 | Robots that use Linux the same way | CI/CD with GitHub Actions |
| 17:00 | Plugging in: /dev, /media and /mnt | mounting drives and network shares, backups |
| 17:30 | When something breaks, find the layer | troubleshooting by layer |
| 17:45 | The map of the day | the directory hierarchy, revisited |
| | Where to go next | a learning path for research computing, with resources for each next step |
| | Sources and scope | references, assumed environment, limitations |

## Getting started

The tutorial is a single self-contained HTML file with no build step and no installation.

1. Download or clone this repository.
2. Open `index.html` in a current web browser (Chrome, Edge, Firefox or Safari).

Light and dark themes are supported, and the animations respect the operating system's reduced-motion setting. Web fonts load from Google Fonts when online; the page falls back to system fonts when offline.

To open a view directly, add `#fs` (file system) or `#story` to the page address.

## Scope and accuracy

This is an introductory, conceptual tutorial, not a hands-on course. The research scripts and data in the story are not included; the page's *Where to go next* section points to resources for practical skills.

The examples describe an Ubuntu-based workstation with Bash and systemd. Commands, file locations and login methods may differ on other Linux distributions, HPC clusters and cloud systems; follow your institution's documentation for cluster resources, storage and software. The tree is a simplified learning model, not a literal map of every interaction. Host names, user names, job IDs and command output in the examples are illustrative.

## Repository contents

| File | Description |
|---|---|
| `index.html` | The complete tutorial: diagrams, animations, story and styles in one file |
| `og-image.png` | Preview image shown when the tutorial link is shared |
| `LICENSE` | MIT licence for the code; the text and diagrams are CC BY 4.0 |
| `README.md` | This document |

## Feedback

Feedback on clarity, accuracy and usability is welcome. Please [open an issue](https://github.com/hossainms/how-linux-works/issues).

## License

- **Text, story and diagrams:** [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/). You may reuse and adapt them with credit to MD Shakhaowat Hossain.
- **Code** (HTML structure, CSS and JavaScript): [MIT](LICENSE).

## Author

**MD Shakhaowat Hossain**
PhD Candidate, Tulane University School of Medicine

Development note: Claude Code was used to translate the author's ideas and technical knowledge into the interactive diagram and accompanying stories.
