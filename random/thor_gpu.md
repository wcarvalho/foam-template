## Setting up Display for XSERVER

#### GLX Gears

* check if `glxgears` is installed with `glxgears -display :0`
* If not, install as follows:

```bash
sudo apt-get install -y xorg xterm xserver-xorg mesa-utils
sudo nvidia-xconfig
```

You might need to edit `/etc/X11/Xwrapper.config` (`sudo vim /etc/X11/Xwrapper.config`)to let anybody start `xinit` by changing

```
allowed_users=console
allowed_users=anybody
```

#### Set-up for using multiple GPUs

* [running AI2Thor on multiple displays](https://medium.com/@etendue2013/how-to-run-ai2-thor-simulation-fast-with-google-cloud-platform-gcp-c9fcde213a4a)
* [how to make xorg.conf](https://askubuntu.com/questions/217758/how-to-make-an-xorg-conf-file)

X11 configuration file /etc/X11/Xorg.conf needs to be created. To assign a screen to each GPU, there should be N screens configured in this file (by default it is only one GPU). 

Generate the x11 config file using the following command:
```
sudo nvidia-xconfig -a --allow-empty-initial-configuration
```
where -a means create screen for all GPUS.  Without the second flag the error screen cannot be found occurs

**How to check this worked:** the following commands should work.

```
xinit&
glxgears -display :0.1
glxgears -display :0.2
glxgears -display :0.3
```

### Change the maximum number of processes (needed for running many instances of Thor)

* CHANGING MAX NUMBER OF PROCESSES
```
  ulimit -u         # checks (should be 4096)
  ulimit -u 65536   # changes
```


