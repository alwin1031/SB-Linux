# Build a Automatic Structural Analysis Pipeline in Ubuntu Server (Chapter 1)
This is a tutorial for installing structural biology programs in Linux (Ubuntu).

Hardware:
HPE Z420 workstation
Intel Xeon E5/Core i7
Storage:
500 GB +500 GB


PLEASE RUN THIS COMMAND everytime you use apt-get to install new package: `sudo apt-get update` to prevent you from seeing `E: Unable to locate package xxx`.


## Install Phenix
1. First, you have to prepare an "academic email account" for Phenix download, Gmail is forbided!
2. Then follow [Phenix doc: Install-setup-run](https://phenix-online.org/documentation/install-setup-run.html).
3. If you feel the installation time is too long, you can always check the size of the installing destination by `sudo du -sh /xxx`.


## Install CCP4 (with Coot)
1. Download link: [CCP4: Linux download](https://www.ccp4.ac.uk/download/#os=linux)
2. Follow [CCP4: installation guideline](https://www.ccp4.ac.uk/download/installation.html)
3. You may missing tcsh, so run `sudo apt-get install tcsh` first.
4. Go to the installer: `cd ~/Downloads`, Unzip: `tar -xvzf linux-x86_64_ccp4-8.0-setup.tar.gz`, Install: `./ccp4-8.0-setup`.
5. run `source bin/ccp4.setup-sh` or `bin/ccp4.setup-csh`.
6. Test Coot in Phenix! If the path of Coot pathway cannot be recognized by the Phenix: try the [Phenix doc: Coot](https://phenix-online.org/documentation/coot.html)
the pathway should be /usr/local/xtal/coot64/bin/coot

## Install ChimeraX
1. You might meet: `ucsf-chimerax : Depends: libffi7 but it is not installable`, you can find the solution here: [Link](https://mail.cgl.ucsf.edu/mailman/archives/list/chimerax-users@cgl.ucsf.edu/thread/ERBZZR5QJBKMFDG3KPPEYWFSOG4O6MH4/#ZX6DNVSPSU2MZKZJMR2X6EA2XNOLY7AQ)
2. This is another method using [Flatpak](https://flatpak.org/setup/Ubuntu), the tutorial is here: [Link](https://www.cgl.ucsf.edu/chimerax/flatpak.html)

### Reference
1. http://ukko.life.nctu.edu.tw/~u0317061/install
2. http://eigenvaluables.blogspot.com/2011/10/installing-ccp4-coot-pymol-and-phenix.html
