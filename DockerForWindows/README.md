# Installing Docker for Windows

Hi, this is an installation guide for using Docker for Windows. 
Currently, the only way for you to use Docker on Windows is through the "Docker for Windows" program provided by Docker. 
However, you can only install it if you have Windows 10 Pro edition on your machine. 
Luckily, you can "trick" the installer if you are running in Windows 10 Home edition and you actually have
virtualization enable on your machine.

## Installation

### Downloading Docker for Windows

This installation only works for an older version of Docker for Windows (2.1.0.5)

Download this specific version [here](https://download.docker.com/win/stable/40693/Docker%20Desktop%20Installer.exe)

### Enable Docker for Windows even when you are on Windows 10 edition

1. Run the ```InstallHyperV.bat``` file in Administration mode. After the installation, it will prompt you to restart. Enter ```N```.

2. Run the ```InstallContainers.bat``` file in Administration mode. 

3. Restart your computer after the last ```.bat``` file have finished running.

Ok great! Now that we have Hyper-V and Containers installed, it is time to trick Docker that we are running on Windows Pro.

### Tricking Docker for Windows that you have a Pro version of Windows installed

1. Press ```Windows + R``` and write ```regedit```.

2. In the Registry Editor, go to ```\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion```.

3. Right-click on **EditionID** and Click **Modify**.

4. Change Value Data to ```Professional```.

5. Press **OK**. (Note: If you restart your computer, the **EditionID** will be reset and you have to set it again).

6. You can resume the installation of the Docker for Windows. If prompted, choose to run on Windows containers for now.

7. After the successful installation, revert back the **EditionID** to its previous value that you have backed up or just restart your machine.

8. Toggle the experimental flag from ```false``` to ```true``` in the Docker Settings.

Based on a post found [here](https://itnext.io/install-docker-on-windows-10-home-d8e621997c1d)

Thanks and Enjoy,
Eron
