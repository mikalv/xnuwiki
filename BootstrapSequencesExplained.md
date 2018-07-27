# Bootstrap sequences

## For i386 / x86_64


### Stage 1

The history starts in a function named "_vstart" in osfmk/i386/i386_init.c on about line 377. Both 32bit and 64bit start the execution from here since at this time, XNU don't need to know if it's 64bit or not yet - only that the architecture is intel based.

If a debugger is detected _vstart will also initialize the serial console code.

The next function to execute is "i386_init" which neither needs to know the max bits yet. This function will setup the required structures and such for an debugger to interact. It also loads the panic screen in case you screw up.

In SMP (multi core) systems the function "i386_init_slave" will be initialized on the "non-main" cores.

The functions "thread_bootstrap", "processor_bootstrap", "power_management_init" and "machine_startup" might be interesting if this area of the kernel is interesting for you.

After all of them are executed, the BSD subsystem is next in line.

### Stage 2

The BSD subsystem. PID 1 will be spawned here.



## For arm / aarch64
