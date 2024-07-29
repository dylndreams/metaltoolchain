# metaltoolchain
(I don't know why I made a repo for this)<br/>
The setuptoolchain script is used to compile/recompile the sh-elf toolchain easily. It is a dependency for the upcoming libLUCID library that I'm working on. However, anything that has a SuperH CPU can use this toolchain.

## usage
Mark it as executable, this can be easily done with
`chmod +x setuptoolchain`. You should also be able to mark it in Files.<br/>

This script provides options to recompile parts such as Newlib, GCC, and Binutils, just in case something (or in my case, Newlib) doesn't compile. This can be done with:
- `./setuptoolchain --gcc`
- `./setuptoolchain --newlib`
- `./setuptoolchain --binutils`

