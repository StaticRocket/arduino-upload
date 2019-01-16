# Arduino Upload Package

[![Greenkeeper badge](https://badges.greenkeeper.io/StaticRocket/arduino-upload.svg)](https://greenkeeper.io/)

Did you not like the look of the Arduino IDE but were stuck with it nevertheless? Not anymore, this package provides some essential features of the Arduino IDE.

* Verify a sketch
* Build a sketch
* Upload a sketch
* Serial Monitor
* Error output when compiling
* Files are clickable in build output --> cursor jumps to that line in that file
* Switch board directly in the status bar

## Installation
`apm install arduino-upload`
(Requires atom 1.10 or later)

## Troubleshooting
* The verify/build output does not appear? Make sure your Arduino official IDE language is set to English.
* Windows
	* Getting `Uncaught Error: spawn EPERM`? Be sure you don't have the Microsoft Store version of the Arduino IDE. - [#65](https://github.com/Sorunome/arduino-upload/issues/65)
	* Can't install because of the serialport package? Try installing the [Visual C++ 2015 building tools](https://github.com/felixrieseberg/windows-build-tools) by running `.\npm install --global --production windows-build-tools` from the directory `%LocalAppData%\atom\app-[VERSION]\resources\app\apm\bin` in an adminastrative PowerShell (this uses atoms integrated npm instead of requiring an external instance). Then update apm config with `apm config set msvs_version [VERSION]` (the version installed by the tool should be 2015) and `apm config set python [PATH]\python.exe` (where PATH is the path to the python executable). - [#46](https://github.com/Sorunome/arduino-upload/issues/46)


## Available commands
* `arduino-upload:verify` - Verifies the sketches (checking for error output), deletes all sources, though
* `arduino-upload:build` - Builds the current sketch, the .hex, .elf, .eep and .bin are copied to the sketch directory
* `arduino-upload:upload` - Uploads the current sketch to a connected arduino
* `arduino-upload:serial-monitor` - Opens the serial monitor of a connected arduino

You can place these commands in a toolbar using the [**Flex Tool Bar**](https://atom.io/packages/flex-tool-bar) package. [Here's how](https://github.com/Sorunome/arduino-upload/blob/master/docs/toolbar.md).

## Screenshots
Verifying a program:

![verify](https://raw.githubusercontent.com/Sorunome/arduino-upload/master/docs/screenshots/verify.gif)

Serial monitor:

![serial](https://raw.githubusercontent.com/Sorunome/arduino-upload/master/docs/screenshots/serial.gif)
