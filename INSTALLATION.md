# Installation

## Building from Source

The provided `install.sh` script will build everything and install it for you. Before running the installation script you have to install the dependencies needed for compiling.

### Build Dependencies

- openSUSE Tumbleweed / Leap 15.6+:

```
sudo zypper install gcc-c++ kf6-extra-cmake-modules \
  kdecoration6-devel kwin6-devel plasma6-framework-devel \
  kf6-kcoreaddons-devel kf6-kconfig-devel kf6-kdeclarative-devel \
  kf6-kpackage-devel kf6-ksvg-devel kf6-ki18n-devel \
  kf6-kservice-devel kf6-kconfigwidgets-devel kf6-kcmutils-devel \
  qt6-gui-devel qt6-qml-devel qt6-quick-devel qt6-dbus-devel qt6-widgets-devel
```

- Ubuntu 24.04+ / KDE Neon:

```
sudo apt install g++ extra-cmake-modules \
  qt6-base-dev qt6-declarative-dev \
  libkf6coreaddons-dev libkf6config-dev libkf6declarative-dev \
  libkf6package-dev libkf6svg-dev libkf6i18n-dev \
  libkf6service-dev libkf6configwidgets-dev libkf6kcmutils-dev \
  libkdecorations3-dev libkwin-dev libplasma-dev gettext
```

- Fedora 41+:

```
sudo dnf install gcc-c++ extra-cmake-modules \
  qt6-qtbase-devel qt6-qtdeclarative-devel \
  kf6-kcoreaddons-devel kf6-kconfig-devel kf6-kdeclarative-devel \
  kf6-kpackage-devel kf6-ksvg-devel kf6-ki18n-devel \
  kf6-kservice-devel kf6-kconfigwidgets-devel kf6-kcmutils-devel \
  kdecoration-devel kwin-devel plasma-framework-devel
```

- Arch:

```
sudo pacman -Syu
sudo pacman -S gcc cmake extra-cmake-modules \
  qt6-base qt6-declarative \
  kf6-kcoreaddons kf6-kconfig kf6-kdeclarative \
  kf6-kpackage kf6-ksvg kf6-ki18n kf6-kservice \
  kf6-kconfigwidgets kf6-kcmutils \
  kdecoration kwin plasma-framework
```

### Building and Installing

Once you have installed the dependencies listed above you can execute the build and install script:

```
sh install.sh
```

### Manual Build

```bash
mkdir build && cd build
cmake -DCMAKE_INSTALL_PREFIX=/usr -DCMAKE_BUILD_TYPE=Release -Wno-dev ..
make -j$(nproc)
sudo make install
```

### Restart Plasma

After installation, restart `plasmashell` to load the applet:

```bash
kquitapp6 plasmashell && kstart plasmashell
```

Then right-click your panel → **Add Widgets** → search for **"Window Buttons"**.

### Uninstalling

```
sh uninstall.sh
```
