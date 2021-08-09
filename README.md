# HoundSploit

![HoundSploit Logo](/HoundSploit/static/media/icon.png)

Author: Nicolas Carolo <nicolascarolo.dev@gmail.com>

Copyright: © 2021, Nicolas Carolo.

Date: 2021-08-09

Version: 2.5.0


## PURPOSE

_HoundSploit_ is an advanced search engine for Exploit-DB developed in
Python using Flask as micro web framework, born with the aim of showing the user
the most accurate search results.

### Features

* Effective version number filtering
* Advanced filtering
* Sort by date and description
* Fast search
* Search suggestions with customization
* Syntax highlighting of the source code of exploits and shellcodes
* Downloading of the source code of exploits and shellcodes
* Highlighting of searched words in search results
* Check for updates (both for software and database)

#### New features in HoundSploit 2
* Flask instead of Django
* SQLAlchemy instead of Django ORM
* The kernel of the search engine is the same used in [_hsploit_](https://github.com/nicolas-carolo/hsploit), which is the CLI version of HoundSploit
* Dark and Light themes

#### Effective version number filtering examples
##### Example I

11 exploits and 0 shellcodes found for "WordPress Core 2.0.2"

![Search example 1](/img/example-1.png)


##### Example II

16 exploits and 0 shellcodes found for "Linux Kernel 4.2.3"

![Search example 2](/img/example-2.png)


#### Advanced filtering

Using advanced search you can use the following filters for filtering search
results:
* Search operator: `AND` or `OR`
* Author
* Type
* Platform
* Port
* Date interval

![Advanced filtering](/img/advanced-filtering.png)


#### Search suggestion

You can choose to show a particular suggestion for a given searched string.
For each case you can also decide to use automatic replacement or not.
It is possible to add new suggestions and delete the existing suggestions.

![Suggestions](/img/suggestions.png)

#### Customization
You can choose to use the Light or the Dark theme

![Light Theme](/img/light-theme.png)

![Dark Theme](/img/dark-theme.png)


## MINIMUM REQUIREMENTS

### Supported OS

* Linux
* macOS
* Windows (Preview)

### Interpreter and tools

* Python 3
* SQLite 3
* git


## INSTALLATION

### Linux (non-root user) [recommended]
In order to install _HoundSploit_ we have to run the following commands:
```sh
$ git clone https://github.com/nicolas-carolo/houndsploit
$ cd houndsploit
$ ./install_db_linux.sh
$ pip install -r requirements.txt
$ python setup.py install
```
Now you can remove the repository of _HoundSploit_ you have downloaded, because this repository has been cloned in `~/.HoundSploit/houndsploit` for supporting automatic updates.
If you have already installed the version 2.1.0 of _hsploit_ or you never installed _hsploit_, you can check if there is the directory `~/HoundSploit` and then you can delete it.

### Linux (root user)
In order to install _HoundSploit_ we have to run the following commands:
```sh
$ git clone https://github.com/nicolas-carolo/houndsploit
$ cd houndsploit
$ mkdir /root/.HoundSploit
$ touch /root/.HoundSploit/enable_root.cfg
$ ./install_db_linux.sh
$ pip install -r requirements.txt
$ python setup.py install
```
Now you can remove the repository of _HoundSploit_ you have downloaded, because this repository has been cloned in `~/.HoundSploit/houndsploit` for supporting automatic updates.
If you have already installed the version 2.1.0 of _hsploit_ or you never installed _hsploit_, you can check if there is the directory `~/HoundSploit` and then you can delete it.

### macOS
In order to install _HoundSploit_ we have to run the following commands:
```sh
$ git clone https://github.com/nicolas-carolo/houndsploit
$ cd houndsploit
$ ./install_db_darwin.sh
$ pip3 install -r requirements.txt
$ python3 setup.py install
```
Now you can remove the repository of _HoundSploit_ you have downloaded, because this repository has been cloned in `~/.HoundSploit/houndsploit` for supporting automatic updates.
If you have already installed the version 2.1.0 of _hsploit_ or you never installed _hsploit_, you can check if there is the directory `~/HoundSploit` and then you can delete it.

### Windows (Preview)
Before proceding with the installation, be sure that you have installed Python from the [official site](https://www.python.org/downloads/) and not from the Windows Store
Run a _PowerShell_ session as _Administrator_
```powershell
PS> git clone https://github.com/nicolas-carolo/houndsploit
PS> cd houndsploit
PS> powershell.exe -ExecutionPolicy Bypass -File .\install_db_windows.ps1
PS> pip install -r requirements.txt
PS> python setup.py install
```
Now you can remove the repository of _HoundSploit_ you have downloaded, because this repository has been cloned in `~\.HoundSploit\houndsploit` for supporting automatic updates.

### Troubleshooting
If you encounter problems during the installation phase, please run:
```sh
$ rm -fr ~/.HoundSploit
```
and then repeat the installation phase.


## USAGE
1. Run _HoundSploit_ server:
   ```sh
   $ houndsploit
   ```
2. Go to `http://localhost:5000`

## COPYRIGHT

Copyright © 2021, Nicolas Carolo.
All rights reserved.

Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions are
met:

1. Redistributions of source code must retain the above copyright
   notice, this list of conditions, and the following disclaimer.

2. Redistributions in binary form must reproduce the above copyright
   notice, this list of conditions, and the following disclaimer in the
   documentation and/or other materials provided with the distribution.

3. Neither the name of the author of this software nor the names of
   contributors to this software may be used to endorse or promote
   products derived from this software without specific prior written
   consent.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS
"AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT
LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR
A PARTICULAR PURPOSE ARE DISCLAIMED.  IN NO EVENT SHALL THE COPYRIGHT
OWNER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL,
SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT
LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE,
DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY
THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT
(INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
