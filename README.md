# VersionLib (vlib)

vlib is a cross platform library format that also includes a linker(vll) that works on any platform for any platform. Its main aim is to allow cross compiling and removing the dependency hells that all operating systems are currently in.

e.g. You create a .c library, and when u try to give that library to someone else, that person now suddenly has to install all kinds of other libraries. Not only that, because that persons system is newer or older, the versions are different. Now there's a compile error or not... might work, but when running his programming in production, it suddenly has unexpected behavior.. etc. etc.

It's a mess. vlib fixes this. Compile your library .o files to a .vlib file, give the .vlib file to someone else. He links his .o files with your .vlib into an executable (or new library). Always works. 0 unexpected behaviour. No dependencies needed. Not even libc.

Supported OS libraries: ELF (.o .so), future: COFF (.dll .lib .exe)

Supported platforms: Linux, Macos, future: Windows

Supported kernels: Linux, Darwin, Windows NT

