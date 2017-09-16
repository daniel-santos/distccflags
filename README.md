# distccflags

A script for computing CFLAGS for use with distcc.  distccflags only works with versions of GCC which have had [pr39851](https://gcc.gnu.org/bugzilla/show_bug.cgi?id=39851) fixed:

  - GCC 6 > 6.4.0
  - GCC 7 > 7.2.0
  - GCC 8+

The basic use case is:
```sh
  ./distccflags -march=native
```
To specify a different compiler, just set the CC environment variable. Example:
```sh
  CC="${HOME}/builds/gcc-dev/gcc/xgcc -B${HOME}/builds/gcc-dev/gcc" ./distccflags -march=native
```

Please report bugs here.
