# MINGW-packages

This repository contains package scripts for MinGW targets to build under MSYS2.

## References

- [MSYS2 website](https://www.msys2.org/)
- [Official packages](https://github.com/msys2/MINGW-packages)

## Using packages

Download or clone the package folder with the scripts to your machine and build for yourself.

Assuming you have a properly installed MSYS2 environment and build tools, you can build any package using the following command:
```sh
    cd ${package-name}
    MINGW_ARCH=mingw64 PKGEXT=.pkg.tar.xz makepkg-mingw -sCL --nosign --skippgpcheck --needed
```
After that you can install the freshly built package(s) with the following command:
```
    pacman -U --needed ${package-name}*.pkg.tar.xz
```

## License

MINGW-packages is licensed under BSD 3-Clause "New" or "Revised" License.
A full copy of the license is provided in [LICENSE](https://github.com/msys2/MINGW-packages/blob/master/LICENSE).
