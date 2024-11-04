# Installing and Configuring a VM (Virtual Machine)


## Install Virtual Box

1. Download Oracle Virtual Box and Extension
   
   From https://www.virtualbox.org/wiki/Downloads download the 1) Virtual Platform Package for the right Operating System (usually windows) and 2) Virtual Box Extension pack after accepting the License agreement.


2. Install Virtualbox by clicking the executable.


3. Go to File/Tools/Extension Package Manager. Click on the plus sign button and select the extension file downloaded.


## Download ISO for selected OS to install as a VM

We recommend using Linux for developing platform. From Linux our choice is Ubuntu, but any other will do, depending oon background, experience, purpose or like/dislike. Inside Ubuntu we recommend the Mate [https://ubuntu-mate.org/] distro because the desktop can be configure to look as other OS without a hassle. Always select the latest LTS version.


## Create a New VM

1. Click on the New Button (Blue Star)

2. In the window that appears enter:
   - Name: Name_of_the_OS + Version + Purpose (Ex. Ubuntu Mate 24.04 Development) (This is only a suggestion.)

   - ISO Image: Click on the arrow to look for ISO of the OS selected.

   - Click to enable "Skip Unattended Installation"

   - Select the hardware tab

     - Give a Base memory of 8192 MB (you could increase or decrease the memory depending on your actual hardware and use of the VM. For a Win 10/11 computer with at least 16GB in ram and 500+GB in disk use 8GB as ram.)

     - Select 2 processors at least. (You could decrease to 1 or increase depending on the above considerations.)

   - Select Hard Disk tab

     - Give at least 100GB of disk (Once again take in account the above considerations but have in mind that you will need at least 50GB to be useful)

   - Click the Finish Button

3. Now click the settings button (Orange cog) (The new VM must be already selected.)

   - Click the General option, then the Advance tab. Change **Shared Clipboard** and **Drag'n'Drop** to Bidirectional.

   - Click the Display option. Move the Video Memory slider all to the right to get 128MB

   - Click the Storage option. At the bottom click on the blue diskette with a plus sign. Select Optical Drive. In the new windows click on the Add Icon, search in the `C:\Programs\Oracle\Virtualbox` the `VBoxGuestAdditions.iso`, select it with double click.

   - Click the Network option. Verify that the Adapter1 is enable.

   - Click OK Button.

4. Click the Green Arrow to run the VM. Let it run.

5. Install OS as needed.

6. Go to View, scale option, then maximize.

7. Wait to finish installing and reboot.
8. If the OS VM is linux 

   - open a terminal <CTRL><ALT>T

   - change to the `/media/<user>/Vbox_GAs_xxx`` by
     
     ```bash
     cd /media/<TAB><TAB>
     ```

     The 2 <TAB> should complete the correct route.

     Run the complementary virtualbox software:

     ```bash
     sudo ./autorun.sh
     ``` 

     For other OS look for the appropriate folder end execute de corresponding file. 

     Doing this in Linux change the resolution of the VM, so it has to be fixed.

     - Go to the On/Off icon on top to the right. Then Displays. Change resolution accorrding to your monitor, select no less than 1360x768 or more.

     - Apply and keep configuration.