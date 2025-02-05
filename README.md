# QEMU Portable

## Description
**QEMU Portable** is a version of **QEMU** that doesn't require installation and allows you to emulate various operating systems on a Windows machine. This portable version allows you to run OS images such as **Windows**, **Android**, **Linux**, and more, easily and quickly without the need for additional installations.

## Requirements
- **Operating System**: Windows 7 or higher.
- **QEMU**: The extracted QEMU files.
- **Operating System Image**: You will need an ISO image or a virtual hard disk of an operating system (e.g., **Ubuntu**, **Windows**, **Android**, etc.).

## How to Use

### 1. **Download and Extract QEMU Portable**
   - Download the latest version of QEMU from [QEMU Portable Releases](https://github.com/ganarcasas/qemu-portable/releases).
   - Extract the files to a folder of your choice.

### 2. **Download an Operating System Image**
   - Download an ISO image of your desired operating system:
     - [Windows 10](https://www.microsoft.com/en-us/software-download/windows10)
     - [Ubuntu](https://ubuntu.com/download/desktop)
     - [Android-x86](https://www.android-x86.org/download)
   - Place the ISO image in the folder where you extracted QEMU.

### 3. **Run the Emulator**
   - You can now run QEMU with the desired ISO image using the following command in your command prompt or terminal:
     ```bash
     qemu-system-x86_64 -m 2048 -cdrom path_to_your_iso.iso -boot d
     ```
   - Replace `path_to_your_iso.iso` with the path to your ISO file.
   - Adjust the `-m` flag to set the amount of RAM (in MB) for the virtual machine.

### 4. **Other Configuration Options**
   - **Create Virtual Hard Drives**: If you need to create a virtual hard disk for installing an operating system, you can do so with the following command:
     ```bash
     qemu-img create -f qcow2 virtual_device.qcow2 20G
     ```
   - **Boot from Virtual Hard Drive**: To boot from an already installed virtual hard disk, use the `-boot c` option instead of `-boot d`.

### 5. **Stopping the VM**
   - To shut down the virtual machine, use the QEMU interface or press `Ctrl + Alt + Del` within the emulated machine.

---

## Common Issues and Solutions

- **The emulator doesn't start or shows errors**:
  - Make sure the ISO image is correctly downloaded and its name is properly specified.
  - Ensure your computer has enough RAM and CPU resources to emulate the operating system.

- **I can't create virtual disks**:
  - Ensure you're running the commands from the folder that contains the QEMU files.

- **Performance is slow**:
  - If your computer has limited resources, reduce the amount of RAM or CPU cores in the command.

---

## License

QEMU Portable is free software distributed under the **Apache License 2.0**. You can use, modify, and distribute this software under the terms of the license. See the [LICENSE](https://www.apache.org/licenses/LICENSE-2.0) for more details.

---

Enjoy emulating with QEMU Portable! If you have any questions or need help, feel free to open an **issue** on this repository.
