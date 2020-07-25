# linbox
Linux development box configs &amp; stuff

After a pristine Ubuntu 20.04 installation on the ONKYO-NB, the following stuff was set up:

Java
----
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
