# metaltoolchain
(I don't know why I made a repo for this)<br/>
The setuptoolchain script is used to compile/recompile the sh-elf toolchain easily. It is a dependency for the upcoming libLUCID library that I'm working on. However, anything that has a SuperH CPU can use this toolchain.

## usage
Mark it as executable, this can be easily done with
`chmod +x setuptoolchain`. You should also be able to mark it in Files.<br/>

This script provides options to recompile parts such as Newlib, GCC, LIBGCC, and Binutils, just in case something (or in my case, Newlib) doesn't compile. This can be done with:
- `./setuptoolchain -g`
- `./setuptoolchain -n`
- `./setuptoolchain -b`
- `./setuptoolchain -lg`


<br>Compiling all can be done with `./setuptoolchain -a`.<br/>

## known issues
On Fedora, GCC pulls its dependencies from a FTP source, which Fedora's wget doesn't support. The only way you can fix this is if you manually go to contrib/download_prerequisites and change the `base_url` variable from 'ftp' to 'https'.<br/>
The automatic cleanup system may messup libgcc building seperately. Just hope everything works first try.<br/>
On Fedora once more, GCC wont build for some reason, usually crashes around the end of configuration. (try installing g++)<br/>


To be honest, that's all there is to it. I'm testing the toolchain with the Dreamcast and I'll have someone on the Saturn. But other than that, Happy baremetal coding :)<br/>

~ LUCiDViSUALS.
