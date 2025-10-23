===========
SEMU README
===========

SUS Sandboxed EMUlator (SEMU) is a generic and open source userspace
emulator and virtualizer based on `QEMU <http://www.qemu.org/>`_.

As SEMU relies on userspace emulation, makes it quite capable on logging
AWD traffic and sandboxing purposes in a restricted setup environment
(e.g. low-privilege users, docker containers).

Building
========

SEMU is multi-platform software intended to be buildable on all modern
Linux platforms, OS-X, Win32 (via the Mingw64 toolchain) and a variety
of other UNIX targets. The simple steps to build SEMU on Ubuntu are:


.. code-block:: shell

  sudo apt-get update
  sudo apt-get install -y --no-install-recommends ca-certificates wget build-essential python-is-python3 python3-venv python3-tomli ninja-build pkg-config libglib2.0-dev libpixman-1-dev
  mkdir build
  cd build
  ../configure --target-list=x86_64-linux-user --static
  make

You'll then get a static binary called `semu-x86_64`.
