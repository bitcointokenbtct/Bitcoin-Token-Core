
Debian
====================
This directory contains files used to package btctd/btct-qt
for Debian-based Linux systems. If you compile btctd/btct-qt yourself, there are some useful files here.

## btct: URI support ##


btct-qt.desktop  (Gnome / Open Desktop)
To install:

	sudo desktop-file-install btct-qt.desktop
	sudo update-desktop-database

If you build yourself, you will either need to modify the paths in
the .desktop file or copy or symlink your btctqt binary to `/usr/bin`
and the `../../share/pixmaps/btct128.png` to `/usr/share/pixmaps`

btct-qt.protocol (KDE)

