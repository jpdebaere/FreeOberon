![Free Oberon screenshot](http://freeoberon.su/images/screenshot.png)

# Free Oberon
* Version 1.0.3
* Riga, June 18, 2019
* Website: [freeoberon.su](http://freeoberon.su/en), [на русском](http://freeoberon.su)

# Installation

## Installation under OS GNU/Linux.

1. Download Free Oberon source code from [freeoberon.su](http://freeoberon.su) in tar.gz format or from the GitHub repo. Note that the archive with the version for Windows is also suitable, because it contains the source code. Extract the archive to your home directory or to another location on the disk. (This tutorial will assume the files are extracted to the home directory.)
2. Using terminal or in any other way, install the following packages:
  * libsdl2-dev
  * libsdl2-image-dev
  * binutils
  * gcc
  * make

  The names of the packages are given in accordance with their names in the Debian GNU/Linux operating system. They are also suitable for Ubuntu, Linux Mint, Raspbian and other.
  To install them, run the following command:
  ```
  apt-get install -y libsdl2-dev libsdl2-image-dev binutils gcc make
  ```
  (This command must be executed with superuser privileges, that is, you must first run `su` and enter the password.)
  On OS Fedora, Red Hat, CentOS and others, the command and package names will differ (one the packages glibc-static or glibc-devel-static might also be required):
  ```
  sudo yum install SDL2-devel SDL2_image-devel binutils gcc make       (not tested!)
  ```
3. Go to the `src` subdirectory and start the compilation:
  ```
  cd ~/FreeOberon/src
  make -f Makefile_linux
  ```
4. (optional) Append the following line to the end of file `~/.bashrc`:
  ```
  alias fo='cd ~/FreeOberon;./FreeOberon'
  ```
  This will allow you to launch Free Oberon using the `fo` command.

## Installation under Windows.

Download the setup porgram in EXE format from [freeoberon.su](http://freeoberon.su), run it and follow the instructions.

Alternatively, you can download a version of Free Oberon in a ZIP-archive (from [freeoberon.su](http://freeoberon.su)), extract it to any place on the disk and (optionally) create a desktop shortcut.

Note. If you want to recompile Free Oberon under Windows from the source code yourself, refer to Appendix A of the [Free Oberon documentation on freeoberon.su](http://freeoberon.su/files/FreeOberon_v1.0.3_en.pdf), [на русском](FreeOberon_v1.0.3.pdf).

# Usage

Run Free Oberon and type in an Oberon program (or open an example program like `Book.Mod`) and press `F9` to compile and run the program.
The module source code files are saved in subdirectory `Programs` and the compiled executable files are saved in `bin`. `data/bin/compile.sh` and `data\bin\compile.bat` are used to compile a program on GNU/Linux and Windows accordingly and can be edited if required.
Since version 1.0.3 it is also possible to compile and run programs that consist of several modules. Put all modules into `Programs` directory, open the main module and press `F9`. If there is an error in one of the modules of your program, the corresponding file will open up and the error will be highlighted. To recompile, focus the main module again and press `F9`.
If module Graph is used, then SDL2 library will be automatically linked to your program.
