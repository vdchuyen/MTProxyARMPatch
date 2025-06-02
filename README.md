# MTProxyARMPatch
Patch for running MTProxy on ARM (including MIPS) and Ampere (on Oracle Cloud)


1) Start installation - clone [this](https://github.com/TelegramMessenger/MTProxy)
2) Install required depencies (view README.md)
3) Go to MTProto directory
4) Import `arm.patch` and `crc32c.patch` also `Makefile`
5) copy io.h to /usr/include/sys
6) Execute this commands:
- `make clean`
- `patch -p1 < arm.patch`
- `patch -p1 < crc32c.patch`
- `make && cd objs/bin`

7) Continue [normal installation](https://github.com/TelegramMessenger/MTProxy#running)
