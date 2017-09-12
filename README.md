![T-Mobile](./images/T-Mobile_NextGen-Magenta.png)

webdev-setup-tools-ruby
=======================

This package is the ruby installation plugin for webdev-setup-tools-core module.

## Installing Npm Package

  npm install webdev-setup-tools-ruby --save

## Purpose
To automate installation and all required system configurations for the Ruby software package. To automate
Ruby Version Manager (RVM) installation and setup on OSX and Linux to support multiple Ruby versions on the same system.
Additionally, to make all installation and configuration cross platform for Windows 7+, OSX, and Linux.
## Configuration

This package should be installed in the
node modules folder located in the root of the project folder.
It determines the packages to install from the "web-dev-setup-tools" field in the package.json in the project root.
This field typically has the following syntax:


```sh
"web-dev-setup-tools": {
  "ruby": {
    "install": "^2.0.0",
    "gems": {
      // gems to install ...
    }
  },
  // other packages to install ...
}
```
## Usage

  Install ruby
  ```sh
  let setup_tools = require('webdev-setup-tools-ruby');
  setup_tools.installRuby();
  ```








### Important Notes

**Note:** In order to install this package, users will need to have administrative access on their computer.

**Note:** Users running Windows must have powershell script execution enabled. Powershell script execution
is disabled by default as a security feature on many windows distributions. Script execution policy
can either be set to "remotesigned" or "unrestricted", although it is recommended to set the
policy to "remotesigned" to maintain the highest level of security.

**Note:**  To view the current powershell execution policy for windows, copy and paste the following command in
a command prompt:

```sh
  powershell.exe -command "get-executionpolicy"
  ```

**Note:**  To view the set the powershell execution policy for windows, copy and paste the following command in
a command prompt:

```sh
  powershell.exe -command "set-executionpolicy remotesigned"
  ```

**Note:** Users running Windows 7 must upgrade to powershell 3.0 ([`Windows Management Framework 3.0`](https://www.microsoft.com/en-us/download/details.aspx?id=34595)).
By default, Windows 7 comes installed with powershell 2.0. Installation typically requires a system restart.
Users running windows 8 and above have all minimum powershell tools installed by default.

**Note:** .net framework version 4.5 or above is required for script execution on Windows.
This is a prerequisite for many modern software packages, but is not present on Windows 7
out of the box.


## Release History

* 1.0.0 Initial release