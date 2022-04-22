![XCompiler](https://github.com/iamlooper/XCompiler/raw/main/xcompiler.png)

# XCompiler

Compile any shell script into a executable binary for Android

## Introduction

**XCompiler™** is a shell script compiler. First of all, it generates a C source code
 The C code is then compiled using CC and linked with both 32 and 64 arch supportable. It is then further processed to create a stripped PIE (Position Independent Executable). The compiled binary is still dependent on the shebang (i.e #!/system/bin/sh). So, somehow **XCompiler™** can not create completely independent binaries.
 
 **XCompiler™** is not a compiler in general. Rather, it obfuscates the original shell script and compile it using CC. Upon execution, it decrypts the code and execute it.

## Setup (Ubuntu only)

```
git clone https://github.com/iamlooper/XCompiler
cd XCompiler
chmod +rwx "$PWD/setup"
./setup
chmod +rwx "/usr/local/bin/xc"
```

**Note**: **XCompiler™** will only work in Ubuntu. Consider, using Ubuntu or you can try free Ubuntu SSH server [here](https://github.com/Sushrut1101/MultiLinux-SSH).

## Usage

```
xc [arguments] # Options
~ $ xc --help
[*] XCompiler™ v0.2 - By LOOPER (iamlooper @ github)
[*] Usage : xc [-a arch - 32 | 64] -b (optional) <inputFileName> -o <outputFileName>                
 -a32   Compile for arm
 -a64   Compile for arm64
 -o     Output file name of the script to compile
 -b     Brutal CC optimizations for max binary performance                         
~ $ xc -a32 test.sh -o test
~ $ file test
test: ELF 32-bit LSB pie executable, ARM, EABI5 version 1 (SYSV), dynamically linked, interpreter /system/bin/linker, stripped
~ $ xc -a32 -b test.sh -o test1
~ $ file test1
test1: ELF 32-bit LSB pie executable, ARM, EABI5 version 1 (SYSV), dynamically linked, interpreter /system/bin/linker, stripped
~ $ ./test
Hello!
```
More features will come soon with more development in this project.

## Support Us

Support us by joining our telegram [channel](https://t.me/loopprojects) and [group](https://t.me/loopchats). You can support furthermore by giving a star to our github [repo](https://github.com/iamlooper/XCompiler).
