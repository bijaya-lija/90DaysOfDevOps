<h1> Linux architecture Diagram:</h1>

<img width="1024" height="1536" alt="image" src="https://github.com/user-attachments/assets/faa664a9-91db-4944-a6e2-8ad3a2d9cf09" />

The core components of Linux (kernel, user space, init/systemd)

<h2>1. Kernel </h2>
Role: The kernel is the heart of Linux. It manages CPU, memory, devices, and system calls.

<b> Responsibilities: </b>

Hardware abstraction (drivers for disk, network, GPU, etc.)

Process scheduling and multitasking

Memory management (paging, virtual memory)

Filesystem handling (ext4, XFS, etc.)

Networking stack (TCP/IP, sockets)

<strong> Key point: Without the kernel, user applications cannot interact with hardware. </strong>

<h2> 2. User Space </h2>
Definition: Everything outside the kernel — applications, libraries, shells, and graphical environments.

Components:

  GNU utilities (bash, coreutils, etc.)

  Libraries (glibc, OpenSSL, etc.)

  Applications (editors, browsers, servers)

  Desktop environments (GNOME, KDE, XFCE)

  Interaction: Programs in user space call kernel functions via system calls (e.g., open(), read(), write()).

 <h2> 3. Init System / systemd </h2>
Init (historical): The first process (PID 1) started by the kernel after boot. Traditionally SysV init, which used runlevels (0–6) to define system states.

systemd (modern): Now the default in most Linux distros.

  Responsibilities:

    Starts as PID 1 after kernel initialization.

    Manages services, sockets, timers, and mounts.

    Provides parallel startup for faster boot.

    Monitors and restarts failed services.

    Defines system states via targets (e.g., multi-user.target, graphical.target).

<img width="912" height="290" alt="image" src="https://github.com/user-attachments/assets/cc6a3232-cb13-4914-ac9d-83eb518aa1ed" />


Alternatives: OpenRC, runit, s6 — used in some lightweight or non-systemd distros.
