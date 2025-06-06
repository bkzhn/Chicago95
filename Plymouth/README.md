## Plymouth boot splash theme

The Windows95 boot theme is based on the template provided by [http://brej.org/blog/?p=174](https://web.archive.org/web/20180210003217/https://brej.org/blog/?p=174)

It is meant to simulate the Windows 95 boot screen and shutdown screen.

If you wish to use a font other than Helvetica as provided by Cronyx Cyrillic, you must change all occurences of "Helvetica Bold 18" in Chicago95.script to your preferred font.

The RetroTux boot theme is based on the xubuntu-logo Plymouth theme.

#### Install instructions for XUbuntu
Copy the theme folder into the Plymouth theme directory.

- `sudo cp -r Chicago95/Plymouth/Chicago95 /usr/share/plymouth/themes/`
- `sudo cp -r Chicago95/Plymouth/RetroTux /usr/share/plymouth/themes/`

Add to default.plymouth

- `sudo update-alternatives --install /usr/share/plymouth/themes/default.plymouth default.plymouth /usr/share/plymouth/themes/Chicago95/Chicago95.plymouth 100`
- `sudo update-alternatives --install /usr/share/plymouth/themes/default.plymouth default.plymouth /usr/share/plymouth/themes/RetroTux/RetroTux.plymouth 100`

Choose the theme to load. (As you run the following command there will be a number assigned to each theme and located in the first column of a list. Use that number to specify the theme and press enter to continue.)

- `sudo update-alternatives --config default.plymouth`

Update initramfs

- `sudo update-initramfs -u`

#### Install instructions for Arch Linux

Install Plymouth to your system ([ArchWiki](https://wiki.archlinux.org/index.php/Plymouth#Installation))

Copy the theme folder into the Plymouth theme directory.

- `sudo cp -r Chicago95/Plymouth/Chicago95 /usr/share/plymouth/themes/`
- `sudo cp -r Chicago95/Plymouth/RetroTux /usr/share/plymouth/themes/`

Set the theme as default to use

- `sudo plymouth-set-default-theme -R Chicago95`
- `sudo plymouth-set-default-theme -R RetroTux`
