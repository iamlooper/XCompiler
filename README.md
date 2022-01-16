![XCompiler](https://github.com/iamlooper/XCompiler/raw/main/xcompiler.png)

# XCompiler

Compile any shell script into a executable binary for Android

## Introduction

**XCompiler™** is a shell script compiler. First of all, it generates a C source code
 The C code is then compiled using CC and linked with both 32 and 64 arch supportable. It is then further processed to create a stripped PIE (Position Independent Executable). The compiled binary is still dependent on the shebang (i.e #!/system/bin/sh). So, somehow **XCompiler™** can not create completely independent binaries.
 
 **XCompiler™** is not a compiler in general. Rather, it obfuscates the original shell script and compile it using CC. Upon execution, it decrypts the code and execute it.

## Setup

```
git clone https://github.com/iamlooper/XCompiler
cd XCompiler
chmod +rwx "$PWD/configure"
./configure
```

**Note** : For now, only [Termux](https://f-droid.org/en/packages/com.termux/) is supported. Download it and run the above commands.

## Usage

```
xc [arguments] # Options
xc -a32 myscript.sh # To create a binary for arm, output file will be generated as a.out
xc -a32 myscript.sh -o executable.bin # Output file will be generated as executable.bin
xc -a64 myscript.sh # To create a binary for arm64, output file will be generated as a.out
xc -a64 myscript.sh -o executable.bin # Output file will be generated as executable.bin
xc -v # To check XCompiler™ version
xc -h # To get information about all given options
```
More features will come soon with more development in this project.

## Support Us

Support us by joining our telegram [channel](https://t.me/loopprojects) and [group](https://t.me/loopchats). You can support furthermore by giving a star to our github [repo](https://github.com/iamlooper/XCompiler).
