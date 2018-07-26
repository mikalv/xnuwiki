# Directory Structure

## From the git repo

  * `config` - configurations for exported apis for supported architecture and platform
  * `SETUP` - Basic set of tools used for configuring the kernel, versioning and kextsymbol management.
  * `EXTERNAL_HEADERS` - Headers sourced from other projects to avoid dependency cycles when building. These headers should be regularly synced when source is updated.
  * `libkern` - C++ IOKit library code for handling of drivers and kexts.
  * `libsa` -  kernel bootstrap code for startup
  * `libsyscall` - syscall library interface for userspace programs
  * `libkdd` - source for user library for parsing kernel data like kernel chunked data.
  * `makedefs` - top level rules and defines for kernel build.
  * `osfmk` - Mach kernel based subsystems
  * `pexpert` - Platform specific code like interrupt handling, atomics etc.
  * `security` - Mandatory Access Check policy interfaces and related implementation.
  * `bsd` - BSD subsystems code
  * `tools` - A set of utilities for testing, debugging and profiling kernel.


