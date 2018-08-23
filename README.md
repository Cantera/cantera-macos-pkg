# Cantera macOS Matlab Interface Builder

This repository runs a Travis CI job to build release installers for the Matlab interface of
Cantera. It uses the [Packages](http://s.sudre.free.fr/Software/Packages/about.html) app by
Stéphane Sudre to build the installer package for distribution. The current version of that app in
this repository is 1.2.3. The source code for the Packages app is on
[GitHub](https://github.com/packagesdev/packages).

To prepare a new release, change the version number on lines 6, 44, and 52 of `.travis.yml`.
Also change the version numbers on lines 830, 1677, 2184, 2772, and 3290 of
`cantera-matlab-interface.pkgproj`.
