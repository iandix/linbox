# linbox
Linux development box configs &amp; stuff

After a pristine Ubuntu 20.04 installation on the ONKYO-NB, the following stuff was set up:

Java (IRPF)
-----------
* Installed JDK-11 via update-alternatives
* Installed JKD-8 via update-alternatives
* JDK-8 was made default Java

VS Code
-------
* Installed VS Code from Microsoft repo as a Debian package (in oposition to a Snap installation)
* Installed Miniconda3 from the Anaconda repo (no conda init, .bashrc adjusted manually)
* No Git installation required in principle (VS Code has Git embedded)

Node
----
* sudo apt install nodejs
* node --version
* sudo apt install npm
* npm --version
* Configuring Node Global Package Installation without sudo:
  - When npm tries to install to globally, it tries to install it's packages to the sensible location of /usr/local/. When you aren't a super user, this gives the warning checkPermissions Missing write access to /usr/local/lib and error Error: EACCES: permission denied, access '/usr/local/lib' and fails. Other package installers (such as Python's pip) already ship, at least on Ubuntu, with a concept of a user-specific local directory of ~/.local/ to replace the global /usr/local/ to avoid such warnings.
  - Step 1: Configure NPM to install your global executables to ~/.local/bin, and the libraries to ~/.local/lib/node_modules/
```console
npm config set prefix ~/.local  
```
  - Step 2: Add ~/.local/bin to your path by adding to the ~/.bashrc
```console
PATH=~/.local/bin/:$PATH  
```
  - To check the global dir changed accordingly:
```console
npm list -g
```
