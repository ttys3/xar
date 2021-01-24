
Unpacking XIP files on Linux


1. Install xar from https://mackyle.github.io/xar/ (or my fork <https://github.com/ttys3/xar>)
2. Install pbzx from https://github.com/NiklasRosenstein/pbzx (or my fork <https://github.com/ttys3/pbzx/>)
  (use `gcc -llzma -lxar -I /usr/local/include pbzx.c -o pbzx` and copy the binary into your PATH)
3. use `xar -xf XIP_FILE -C /path/to/extract/to`
4. Change to the directory where you extracted the file.
5. Use `pbzx -n Content | cpio -i` to extract the contents.


ref: <https://gist.github.com/phracker/1944ce190e01963c550566b749bd2b54>
