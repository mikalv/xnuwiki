# Directory Structure

## Map

  * `config` - configurations for exported apis for supported architecture and platform
  * `SETUP` - Basic set of tools used for configuring the kernel, versioning and kextsymbol management.
  * `EXTERNAL_HEADERS` - Headers sourced from other projects to avoid dependency cycles when building. These headers should be regularly synced when source is updated.
  * `libkern` - C++ IOKit library code for handling of drivers and kexts.
    * `c++` - Implementation of the "stdlib" of C++ in the kernel.
    * `conf` - BSD alike conf directory for the libkern part of the kernel.
    * `crypto` - Some few cryptographical functions.
    * `kmod` - This is the C++ runtime.
    * `libkern` - The header directory for libkern.
    * `uuid` - A uuid implementation.
    * `zlib` - zlib functions.
  * `libsa` -  kernel bootstrap code for startup
    * `conf` - BSD alike conf directory for the startup part of the kernel.
  * `libsyscall` - syscall library interface for userspace programs
    * `mach` - Code related to the execution of userland binaries.
  * `libkdd` - source for user library for parsing kernel data like kernel chunked data.
  * `makedefs` - top level rules and defines for kernel build.
  * `osfmk` - Mach kernel based subsystems
    * `arm` - Architecture spesific code.
    * `chud` - The Computer Hardware Understanding Development tools.  
    * `conf` - BSD alike conf directory for the mach subsystems of the kernel.
    * `console` - The serial console implementation and panic UI.
    * `corecrypto` - Some more cryptographical functions.
    * `default_pager` - VM Pager.
    * `i386` - Architecture spesific code.
    * `device` - Mach support for I/O Kit and devices.
    * `ipc` - The code for the Interprocess Communication (IPC) system.
    * `kdp` - KDP (Debugger) support.
    * `kern` - Inner Mach code (scheduler, ipc, threading, timers, clock).
    * `libsa` - Mach headers related to startup.
    * `man` - HTML manuals.
    * `prng` - A random number generation implementation.
    * `UserNotification` - Kernel-User Notification (KUNC). 
    * `vm` - Mach virtual memory code.
    * `x86_64` - Architecture spesific code.
  * `pexpert` - Platform specific code like interrupt handling, atomics etc.
  * `security` - Mandatory Access Check policy interfaces and related implementation.
  * `bsd` - BSD subsystems code
    * `bsm` - Basic Security Module (auditing subsystem).
    * `arm` - Architecture spesific code.
    * `conf` - BSD alike conf directory for the bsd subsystems of the kernel.
    * `i386` - Architecture spesific code.
    * `kern` - Inner core BSD code.
    * `man` - BSD manuals.
    * `net` - Code for basic networking.
    * `netinet` - TCP/IP v4 implementation.
    * `netinet6` - TCP/IP v6 implementation.
    * `nfs` - NFS support.
    * `vfs` - Virtual File System layer.
    * `vm` - Unix virtual memory mapper.
  * `tools` - A set of utilities for testing, debugging and profiling kernel.


