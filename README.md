*************************************************************************************************************************
*  TMDL - Telegram DL                                                                                                   *
*                                                                                                                       *
*  VERSION 0.0.4                                                                                                        *
*                                                                                                                       *
*  A tool for Linux, MacOS and Windows to assist creating backups of your favorite channels via the Telegram API        *
*                                                                                                                       *
*  Idea/Written by Sebastian Vivian Gresser                                                                             *
*                                                                                                                       *
*  install modules: pip3 install telethon asyncio tqdm argparse                                                         *
*                                                                                                                       *
*  Usage example:   python3 tmdl.py --id 1234 --hash "1289u3jo1imn" --target "name" --output "directory"                *
*                   python3 tmdl.py --id 1234 --hash "1289u3jo1imn" --target id --output "directory"                    *
*                                                                                                                       *
*                   you will get prompted to type in your phone/bot token                                               *
*                                                                                                                       *
*                   phone token: your phonenumber (e.g. +0155516213576) -> next type in the validation code you         *
*                   just received (you will have to do this once until you delete the registered session)               *
*                                                                                                                       *
*                   bot token: can be generated by talking to the Botfather                                             *
*                                                                                                                       *
*  API ID/HASH URL: https://my.telegram.org/apps (open the link in a browser -> login and create your app to            *
*                   get a app ID/HASH)                                                                                  *
*                                                                                                                       *
*************************************************************************************************************************

Install / Dependencies Instructions:

Linux:
    Debian/Ubuntu:  apt-get install python3 python3-pip
    Gentoo:         emerge python dev-python/pip
    Fedora:         yum install python3 python3-pip
    Arch:           pacman -S python python-pip
    Suse:           zypper install python3 python3-pip

    --> sudo pip3(or pip) install telethon asyncio tqdm argparse
    (locally with: pip3(or pip) install telethon asyncio tqdm argparse --user)

    python tmdl.py --id 1234 --hash "1289u3jo1imn" --target "name" --output "/path/to/download/dir"
    --> or
    python tmdl.py --id 1234 --hash "1289u3jo1imn" --target id --output "~/Downloads"
    --> see
    python tmdl.py for all options

MAC:
    Download a python3 release: https://www.python.org/downloads/macos/
    --> Double-click python.mpkg
    --> Click "Continue" three times
    --> Select the Volume/HD installation target
    --> Click "Install"
    --> Click "Close"
    --> Open a terminal and type: python3 -m ensurepip --> Enter
    --> type: pip3(or pip) install telethon asyncio tqdm argparse

    python tmdl.py --id 1234 --hash "1289u3jo1imn" --target "name" --output "/path/to/download/dir"
    --> or
    python tmdl.py --id 1234 --hash "1289u3jo1imn" --target id --output "~/Downloads"
    --> see
    python tmdl.py for all options

Windows:
    Download a python3 release: https://www.python.org/downloads/windows/ (installer)
    --> Execute the installer file
    --> select the "Install launcher for all users" and "Add Python 3.x to PATH" checkboxes
    --> Click "Install Now"
    --> Check "Disable path length limit" (if you want to allow path-/filenames longer than 260 characters)
    --> Open the Start menu and type "cmd"
    --> Select the "Command Prompt" application
    --> type: py -m ensurepip --upgrade
    Environment Settings:
    --> Open the "Start menu" and start "Run app"
    --> Type sysdm.cpl and click "OK". (opens the System Properties window)
    --> Navigate to the "Advanced" tab and select "Environment Variables"
    --> Look for "System Variables" and select the "Path variable" -> Edit
    --> Select "Variable value" and add ;C:\Python3x at the end
    (x stands for the subversion you installed; e.g. ;C:\Python310 or ;C:\Python39)
    --> Click "OK" -> Now you can execute scripts like tmdl.py by using the Command Prompt -> python tmdl.py

    python tmdl.py --id 1234 --hash "1289u3jo1imn" --target "name" --output "C:\your\download\directory"
    --> or
    python tmdl.py --id 1234 --hash "1289u3jo1imn" --target id --output "C:\your\download\directory"
    --> see
    python tmdl.py for all options

TODO:
	- Use lock files to prevent several processes working on the same file in case the destination folder is the same.
	- Backup messages along with files and create an index in json/html/xml/etc.
	- Plugins for backing up the content of links pointing to video streaming platforms and comparable


*************************************************************************************************************************
*  TMDL GUI - Telegram DL GUI                                                                                           *
*                                                                                                                       *
*  VERSION 0.0.1                                                                                                        *
*                                                                                                                       *
*  A GUI for to ease up controlling several backup processes                                                            *
*                                                                                                                       *
*  Idea/Written by Sebastian Vivian Gresser                                                                             *
*                                                                                                                       *
*  install modules: pip3 install tkinter tkcalendar subprocess                                                          *
*                                                                                                                       *
*  Usage example:   python3 tmdl_gui.py                                                                                 *
*                                                                                                                       *
*                   there is an example queue config file included (tmdl_queue)                                         *
*                                                                                                                       *
*************************************************************************************************************************

TODO:
	- Observe the (overall) progress of a process and display it with an animation (progressbar / ticker / ...)
	- Including new options which will come available with the completion of the TODO tasks of TMDL
