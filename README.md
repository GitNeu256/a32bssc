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
