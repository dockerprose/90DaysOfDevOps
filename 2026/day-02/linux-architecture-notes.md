# Core Component of Linux
1. **Bootloader** : it is responsible for checks memory, ram ,gpu running properly  [GRUB].
2. **Kernel** : after booting all control transfer on Kernel, this is the core of OS.

    **Core Kernel Responsibilities :**
   - Process management
   - Memory management
   - File management
   - Networking
   - Device drivers

3. **Init(systemd)** : it's bootstraps the system that manages *User Space*, it's PID 1
  - Manages services,mount points, and login sessions.
  - cmd for mgmt and troubleshooting: **systemctl** , **journalctl**

4. **User space** : in this space all non-kernel processes executes, Web browsers to low level daemons
  - users can interact with kernel by shell, or system calls
  - it is the memory area where application and background services run


# Process
  - Process is an instance of a program in *execution*
  - and every process has it's own unique id , **PID**
    ## two-step mechanism to create:
      - Cloning(fork) - parent create a copy called child
      - replacing(exec) - replace or share to exec() family.

    ## Manage Processes:
      - ps aux
      - top or htop
      - kill
      - nice/renice
      - command **&**
      - bg/fg -- for job control
