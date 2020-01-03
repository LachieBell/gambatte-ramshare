# gambatte-speedrun

Fork of https://github.com/pokemon-speedrunning/gambatte-speedrun which is a fork of https://github.com/sinamas/gambatte with with ram-share capabilities. Under GPLv2.

Tips for building (on windows with msys2):
    Use qt5 version mingw-w64-x86_64-qt5-static-5.10.1
    Use openssl version mingw-w64-x86_64-openssl-1.0.2
You can download these packages from [here](http://repo.msys2.org/)



This has been updated to build using Qt5 instead of Qt4. If you have Qt5 dependencies, building should be easy enough. It can be built on windows using [msys2](https://msys2.github.io/) and the qt5-static package.

To build it on Debian, do:

    sudo apt install build-essential git scons zlib1g-dev qt5-default libqt5x11extras5-dev libxrandr-dev libxv-dev libasound2-dev
    git clone https://github.com/Dabomstew/gambatte-speedrun
    cd gambatte-speedrun
    sh scripts/build_qt.sh
    cp gambatte_qt/bin/gambatte_qt SOMEWHERE/gsr # or w/e
    
To build the "non-PSR" version with additional selectable platforms (GB, GBC, GBA, SGB2), create `gambatte_qt/src/platforms.pri` with the following:
    
    # platform support
    # GBP is hardcoded
    DEFINES += SHOW_PLATFORM_GB
    DEFINES += SHOW_PLATFORM_GBC
    DEFINES += SHOW_PLATFORM_GBA
    DEFINES += SHOW_PLATFORM_SGB

Otherwise GLHF.
