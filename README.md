Builds for both toolchains using unmodified SYMPHONY-5.6.14.

For RSymphony link with:

    PKG_LIBS = -lSym -lCgl -lOsiClp -lClp -lOsi -lCoinUtils -lz -fopenmp

Note that the old toolchain does not have libz so we include a copy of libz.a
