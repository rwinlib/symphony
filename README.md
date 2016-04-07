symphony compiled with sources from http://www.stats.ox.ac.uk/pub/Rtools/goodies/sources/SYMPHONY-5.6.13.tar.xz

The 32- and 64-bit versions are made separately under W{32,64}soft, and then
merged (the 32-bit libs copied to lib/i386, the 64-bit libs to lib/x64). The
include files are common.

64 bit compilation commands
```bash
./configure --enable-static --disable-shared --prefix=.../W64soft/ --build=x86_64-w64-mingw32 && \
  make && \
  make install
```

32 bit compilation commands
```bash
patch -p < symphony.patch
./configure --enable-static --disable-shared --prefix=.../W32soft/ --build=i686-w64-mingw32 && \
  make && \
  make install
```

To install Rsymphony set `SYMPHONY_HOME` to the directory with the extracted
files, they also seem to require linking against `-lz -fopenmp`.
