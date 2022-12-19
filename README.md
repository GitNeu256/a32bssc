# a32bssc
Simple OS
a32bssc - advanced 32bit system super cool

# Compile 
1. nasm -f elf32 kernel.asm -o kasm.o
2. gcc -m32 -c kernel.c -o kc.o
   gcc -fno-stack-protector -m32 -c kernel.c -o kc.o
3. ld -m elf_i386 -T link.ld -o kernel kasm.o kc.o

# Run in QEMU
qemu-system-i386 -kernel kernel

# Windows build 
1. Install WSL
   PowerShell: wsl --install
2. Then install the version of the Linux distribution you are interested in in the Microsoft Store
3. Register there
4. Run the following commands for better compilation
   sudo apt update
   sudo apt upgrade
   sudo install nasm
   sudo install gcc
5. Execute actions from compile point
   
# Windows Test
1. Install QEMU from the official site (https://www.qemu.org/download/#windows)
2. Execute actions from "Run in QEMU" point 
