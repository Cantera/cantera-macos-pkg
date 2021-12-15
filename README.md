# Cantera macOS Matlab Interface Builder

This repository runs a GitHub Actions job to build installers for the Matlab interface of
Cantera. It uses the [Packages](http://s.sudre.free.fr/Software/Packages/about.html) app by
Stéphane Sudre to build the installer package for distribution. The current version of that app in
this repository is 1.2.10 (development build from [Nov. 26, 2021](https://github.com/packagesdev/packages/issues/97#issuecomment-947189086)). At least this version is required to support Apple Silicon/M1/ARM architecture. The source code for the Packages app is on
[GitHub](https://github.com/packagesdev/packages).

To make a new release, change the `ref` key for the Cantera checkout action to point to the appropriate branch/tag.
That should be on line 26 of `.github/workflows/main.yml`.
Open `cantera-matlab-interface.pkgproj` with the version of Packages from this repository installed
locally on your computer and edit all the version numbers. Also change the environment name
in `support_files/readme.rtf`. Make sure not to remove end-of-line spaces in the `readme.rtf` file.

The workflow creates an artifact for each job that contains the built pkg file.

## License for Packages app

Copyright (c) 2008-2019, Stephane Sudre All rights reserved.

Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:

    Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
    Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
    Neither the name of the WhiteBox nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT OWNER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
