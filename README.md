Builds for both toolchains using unmodified SYMPHONY-5.6.14.

These are compiled with:

    configure --without-openmp

For RSymphony link with:

    PKG_LIBS = -lSym -lCgl -lOsiClp -lClp -lOsi -lCoinUtils -lz

Note that the old toolchain does not have libz so we include a copy of libz.a
