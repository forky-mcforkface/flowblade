# Installing Flowblade

  * [Installing deb package](./INSTALLING.md#installing-deb-package)
  * [Installing Flatpak from Flathub](./INSTALLING.md#installing-flatpak-from-flathub)
  * [Installing from your OS repository](./INSTALLING.md#installing-from-your-os-repository)
  * [Installing using Development Repository Version](./INSTALLING.md#installing-using-development-repository-version)
  * [Installing with setup.py not supported](./INSTALLING.md#installing-with-setuppy-not-supported)   
      
### Installing deb package

#### Step 1. Download and install .deb

**NOTE: Flowblade now requires MLT 6.18 that is NOT available on e.g. Ubuntu 18.04. The reason for this situation is the recent move to Python3.**

**First download .deb file** for Flowblade 2.8.0.2 from <a href="https://github.com/jliljebl/flowblade/releases">here.</a>

Double click on <b>.deb</b> file to install it. 

On some systems double clicking may not work and you need to install <b>.deb</b> file using terminal:

<ul>
    <li>    <p>Open terminal in the directory you saved the  downloaded <b>.deb</b> file. Give command:    </li>
</ul>

    sudo apt install ./flowblade-2.8.0.2-1_all.deb

### Installing Flatpak from Flathub

#### 1. Setup Flatpak and Flathub

There is an official guide here: https://flatpak.org/setup/

#### 2a. Install using Gnome SOFTWARE

If your distribution has Gnome SOFTWARE application available you can install Flowblade with it.
**NOTE: There can be two versions of Flowblade in Gnome SOFTWARE, Flatpak version has text dl.flathub.org text**

#### 2b. Install from commandline

Give these commands in terminal:

```bash
flatpak install --from https://flathub.org/repo/appstream/io.github.jliljebl.Flowblade.flatpakref
```

```bash
flatpak run io.github.jliljebl.Flowblade
```

#### Flatpak missing few features

Unfortunately some features are not available via Flatpak install yet.

* Batch Render Queue does not work
* Blender Container Clips are not available

We are working towards solving these issues.

### Installing from your OS repository

The easiest way to install Flowblade is using the version in your OS repository. The downside is that **the version available may not be the current latest release**. Contact your OS to get latest Flowblade included in repositories if not already available.

#### Ubuntu, Debian and Linux Mint

```bash
sudo apt-get install flowblade
```

#### Archlinux

_Latest release_. Visit the <a href="https://archlinux.org/packages/community/any/flowblade/">AUR</a> page or use terminal command:

```bash
yaourt -S flowblade
```

_Git version_. Visit the <a href="https://aur.archlinux.org/packages/flowblade-git/">AUR</a> page or use terminal command:

```bash
yaourt -S flowblade-git
```

### Installing using Development Repository Version

Flowblade requires MLT 6.18. If this is not available on your distirution Python 3 bindings have to be build and installed to run repository Flowblade. We have some pointers here: https://github.com/jliljebl/flowblade/blob/master/flowblade-trunk/docs/creating_user_folder_bindings.md 

Flowblade is currently a 100% script application, and all the dependencies should be available in popular distributions, so in most cases it should be possible to install and run Flowblade without compiling anything.

Developer version may however be unstable or have new dependencies. If you fail to install developer version, please file a bug in Issues -tab.

* Install Git in your system (Ubuntu command):
  
  ```bash
  sudo apt-get install git
  ```
* Use Git to download Flowblade into a folder of your choosing by using the git clone command in your terminal:
  
  ```bash
  git clone https://github.com/jliljebl/flowblade.git
  ```
* Install dependencies. See   [Dependencies](DEPENDENCIES.md) doc for more information.
* If you have Flowblade installed in your system, you probably have the dependencies installed, unless some new ones have been added.
* Launch by running script ``.../flowblade-trunk/flowblade`` that was created in the folder where clone command was done.
* Note that if you have Flowblade installed you will need use full path to repository version or navigate to the folder containing launch script and use command "./flowblade" to launch repository version instead of installed version

### Installing with setup.py not supported

*Please note: Using the available setup.py script will probably NOT result in a successful installation, even if dependencies are installed, and may actually break the .deb install if attempted. It is only there to help .deb and Flatpak packaging.* 
