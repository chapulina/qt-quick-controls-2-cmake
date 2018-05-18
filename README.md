# Build instructions for Ubuntu 18.04

Dependencies

    sudo apt-get install -y \
        build-essential \
        cmake \
        qtbase5-dev \
        qtdeclarative5-dev \
        qml-module-qtquick2 \
        qtquickcontrols2-5-dev \
        qml-module-qtquick-controls\
        qml-module-qtquick-controls2

Project

    mkdir build
    cd build
    cmake ..
    make -j8

Run

    ./src/Example
