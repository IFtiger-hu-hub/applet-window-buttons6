# Window Buttons Applet

This is a Plasma 6 applet that shows window buttons in your panels. This plasmoid is coming from [Latte land](https://phabricator.kde.org/source/latte-dock/repository/master/) but it can also support Plasma panels.

<p align="center">
<img src="https://i.imgur.com/4FItfte.gif" width="580"><br/>
<i>slide in/out animation</i>
</p>

<p align="center">
<img src="https://i.imgur.com/70qeMME.png" width="580"><br/>
<i>Breeze decoration</i>
</p>

<p align="center">
<img src="https://i.imgur.com/uEen6P0.png" width="580"><br/>
<i>BreezeEnhanced decoration</i>
</p>

<p align="center">
<img src="https://i.imgur.com/Zz20RXC.png" width="580"><br/>
<i>Settings window</i>
</p>

# Requires

- Qt >= 6.6.0
- KF6 >= 5.246.0
- Plasma >= 5.90 (Plasma 6)
- KDecoration3 >= 6.2.90
- KWin (for DBus interface `org.kde.KWin.xml`)

**Qt elements**: Gui Qml Quick DBus Widgets

**KF6 elements**: CoreAddons Config Declarative Package Svg I18n Service ConfigWidgets KCMUtils

**Runtime QML dependencies**: org.kde.taskmanager (from plasma-workspace), org.kde.kirigami, org.kde.kitemmodels

# Install

You can execute `sh install.sh` in the root directory as long as you have installed the previous mentioned development packages. For more details please read [INSTALLATION.md](/INSTALLATION.md)
