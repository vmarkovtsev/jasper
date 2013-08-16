Jasper
======

Stripped Jasper (JPEG2000 library) with fixed 64-bit portability issues and various security patches applied, compiled with cmake.

Building
--------

    mkdir build
    cd build
    cmake ..
    make -j8
    
What was changed
----------------

* Only jp2 and jpc codecs were left;
* Fixed int_fast32_t and friends formatting in printf-like functions on 64-bit platforms
* Applied Debian patches (except alloc2/realloc2)
* Applied patches from [abveritas](https://github.com/abveritas/main/tree/master/jasper)
* Ensured sleek compilation with -Wall
* Changed build system to cmake
