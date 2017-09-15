AstroBox Software - Orange Pi Zero Port
=================

The AstroBox software provides a responsive web interface for controlling a 3D printer (RepRap, Ultimaker, ...) and connecting to the AstroPrint cloud for easy 3D Printing anywhere. It is Free Software and released under the [GNU Affero General Public License V3](http://www.gnu.org/licenses/agpl.html).

This Orange Pi Zero port project started as a branched fork of [AstroBox](https://github.com/AstroPrint/AstroBox). Many thanks to Astroprint Team and all the great contributors there that made the AstroBox software possible.

Its website can be found at [astroprint.com](https://www.astroprint.com).

Reporting bugs
--------------

The Orange Pi Zero issue tracker can be found [on Github](https://github.com/moracabanas/AstroBox/issues).


Installation instructions
-------



* Download a Armbian 5.30 bootable image using the image from [Armbian](https://dl.armbian.com/orangepizero/Ubuntu_xenial_default.7z)

* Make a SD card bootable with [Etcher](https://etcher.io/)

* Connect your Orange Pi Zero to your PC, wait a minute. A new device will be found just look for the COM port and take note. (On Windows you can use Device Manager).

* Use your preferred SSH App to access the found COM port which gives you instant command line to your Orange Pi. I Use [Putty](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html) on Windows.

* Once on the Armbian command line log-in as: <pre> 
    User:     root 
    Password: 1234
    </pre>

* Create your user account, Armbian will ask you as soon as you log-in.

* Reboot to resize file system as indicated.

<pre>
$ reboot
</pre>

* Log-in with your user.

* Connect to your network, with ethernet cable or use:
<pre> * $ nmtui </pre> and follow the easy interface.

* Download the source code.

  <pre>
    git clone https://github.com/moracabanas/AstroBox.git -b orange-pi-zero-port && cd AstroBox/source && sudo make
  </pre>

After the download the Installation script will install all the dependencies and source files):

It will take some time, maybe half an hour, and it promts you sometimes for user confirmation. Be patient :D

### Execute Astroprint for the first time

<pre>
  $ sudo sh ./runAstroprint
</pre>

* Find your ip with ifconfig and loking for the wlan0 interface IP.

### Go to your browser with your IP and enjoy Astrobox on your Orange Pi Zero.

* I strongly reccomend to perform and update and a factory reset from the web interface as there is some issues we have to solve.
