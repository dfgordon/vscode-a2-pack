# Apple II Pack

This is a set of extensions that are useful for those interested in cross developing for retro computers, especially the Apple II.  They can also be helpful for archivists, or anyone just interested in old software.  The extensions in the pack are not interdependent, i.e., you can install them separately if you prefer.

## Core Language

`Applesoft BASIC`, `Integer BASIC`, and `Merlin 6502` provide complete language server support for the respective Apple II languages.

`Pascal Language Basics` will highlight a UCSD Pascal file.  You may also like to check out `Pascal`, which provides additional services, but may require some configuring.

## Disk Images

`Disk Image Notebook` provides a convenient interface for browsing a disk image.  If disk images are produced as part of a build process, this can be used to inspect the results without ever leaving the editor.  It can also be used as a convenient way to load files from a disk image into the editor.

The BASIC and Merlin language extensions provide their own independent capability for accessing disk images.

## Extras

`Insert Unicode` is useful for inserting control characters directly into your BASIC code.

`AppleScript` is useful if you would like to script the Virtual II emulator.

`PowerShell` is useful for deploying files to a disk image within two clicks, assuming you develop a script for this.  Typically the script runs some command line tool (e.g. [a2kit](https://github.com/dfgordon/a2kit)) in a subprocess.  

## File Extension Collisions

If you use `.bas` for all BASIC dialects, you will likely have problems when more than one BASIC dialect is enabled at the same time.  The following strategies can be used to mitigate this issue:

* Use `.abas` for Applesoft and `.ibas` for Integer.  The drawback is other software will not recognize the files as BASIC (e.g., Github will display wrong statistics about your project).
* Use VS Code file associations to strongly associate `.bas` with the dialect of your choice.  This is effective if you are predominantly using one dialect.
* Disable the extension that handles the dialect you are not using during a given campaign.

As of this writing, the language mode button is not effective for switching dialects.  The problem is switching language modes does not cause existing diagnostics to be removed.

## Platform Support

The BASIC, Merlin, and Disk Image extensions should work out of the box for typical Windows, Linux, and Mac systems.  In case of an atypical system (say, Windows on arm64), these extensions can still be used, but you will have to install [a2kit](https://github.com/dfgordon/a2kit) separately.  If you have the rust toolchain, this is usually as simple as entering `cargo install a2kit` in the terminal.