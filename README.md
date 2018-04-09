# Mattermost Desktop

Native desktop application for [Mattermost](http://www.mattermost.org/) running on Windows, Mac, and Linux.

Originally created as "electron-mattermost" by Yuya Ochiai. Developed using [Electron](http://electron.atom.io/).

![screenshot_20](https://user-images.githubusercontent.com/29708087/35169141-65d7652a-fd29-11e7-901d-735881fb7b9d.png)

[![Circle CI](https://circleci.com/gh/mattermost/desktop.svg?style=shield)](https://circleci.com/gh/mattermost/desktop)

## Features

### Desktop integration
* Tabs for multiple teams across multiple servers
* Desktop Notifications
  * Windows 10: Toast
  * Windows 7-8.1: Popup like Toast
  * OS X: Notification Center
  * Linux: [libnotify](http://electron.atom.io/docs/v0.36.0/tutorial/desktop-environment-integration/#linux)
* Badges for unread channels and mentions
* Installs as native application

### Pre-packaged
You don't have to install any other software.
Packages are available on the [releases page](http://github.com/mattermost/desktop/releases).

## Usage

### Installation
Detailed guides are available at [docs.mattermost.com](https://about.mattermost.com/default-desktop-app-documentation/).

1. Download a file from the [downloads page](https://about.mattermost.com/downloads).
2. Launch `Mattermost` in the unarchived folder.
3. After first launching, please input name and URL for your Mattermost server. For example, `myserver : https://mattermost.example.com`.

### Quit
Ctrl or Command + Q to quit.

### Configuration
You can show the dialog from menu bar.

Configuration will be saved into Electron's userData directory:

* `%APPDATA%\Mattermost` on Windows
* `~/Library/Application Support/Mattermost` on OS X
* `~/.config/Mattermost` on Linux

*When you upgrade from electron-mattermost, please copy `config.json` from `electron-mattermost`.
Otherwise, you have to configure again.*

### Proxy
Normally, the application will follow your system settings to use proxy.
Or you can set proxy by following command line options.

* `--proxy-server=<SERVER>:<PORT>`
* `--proxy-pac-url=<URL>`

On Windows, please make sure adding `--` before options. For example, `Mattermost.exe -- --proxy-server=...`.

## Contributing
Please see [CONTRIBUTING.md](./CONTRIBUTING.md).

## Development
Please see [docs/development.md](./docs/development.md).
