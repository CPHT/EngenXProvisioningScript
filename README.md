# GPS Provisioning Script

## Table of contents
- [Download](#download)
- [Prerequisites](#prereq)
- [Mac Printer Setup](#printermac)
- [Script Usage](#run)
- [References](#ref)
- [Extras](#extra)

<div id='download'/>

## How to download the script
- *ENTER* in Terminal
  - `git clone https://github.com/tmeserve/ProvisioningScript.git`
- Switch to `nocups` branch
  - `git checkout nocups`

<div id='prereq'/>

## Prerequisites
- Install [python 3.7.2](https://www.python.org/downloads/release/python-372/)
  - To get help with installing python 3.7.2 on mac go to [here](https://www.youtube.com/watch?v=8BiYGIDCvvA)
- _Pip usage_
  - *ENTER* in Terminal
    - Change into the directory of the cloned repository
      - `cd user/yourName/EngenxProvisioningScript`
    - Create a virtual environment in this directory
      - `python3 -m venv .`
    - Install required libraries
      - `pip3.7 install -r requirements.txt`
- _Drivers_ (macOS 10.11 - 10.14)
  - Install the [drivers](https://docs.microsoft.com/en-us/sql/connect/odbc/linux-mac/installing-the-microsoft-odbc-driver-for-sql-server?view=sql-server-2017#os-x-1011-el-capitan-macos-1012-sierra-macos-1013-high-sierra-and-macos-1014-mojave) according to your operating system.
    - Install Homebrew
      - `/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`
    - Tap and install drivers and tools
      - `brew tap microsoft/mssql-release https://github.com/Microsoft/homebrew-mssql-release`
      - `brew update`
      - `brew install msodbcsql17 mssql-tools`
  - Install IOgear GUC232A USB to serial adapter driver (optional)
    - https://www.iogear.com/support/dm/driver/GUC232A

<div id='printermac'/>

## To set up the printer on a Mac
- *PLUG IN* the printer through the serial port to usb

<div id='run'/>

## Running the Script
- *ENTER* in Terminal
  - Change into the directory of the cloned repository
    - `cd user/yourName/my-project`
  - `python3.7 runner.py`

<div id='ref'/>

## Credit
- [John Cobb](https://github.com/johncobb/cfgmdm)
- [Venv Installation](https://virtualenv.pypa.io/en/stable/installation/)
- [Venv Usage](https://virtualenv.pypa.io/en/stable/userguide/)

<div id='extra'/>

## Extra Information
- The COM Port is the name or location of the serial port.
