# Setup Jetson TX2 with Host Computer

## **I. Install ubuntu. You can follow [Link here](https://github.com/Linhndm/Install_ubuntu).**
***Hint**:Your Jetson TX2 will use Ubuntu version of the same Host computer.*

***Note: I will use ubuntu 18.04 and last verrsion jetpack(4.4)***

## **II. Install Nvidia SDK Manager in the host computer and turn on Recovery Mode from TX2**
### **Step 1: On the host computer**:



1. Link Install [Nvidia SDK Manager](https://developer.nvidia.com/embedded/downloads)

2. Choose NVIDIA SDK MANAGER and download the install file. Run install file and install SDK Manager on the host computer



### **Step 2: On the TX2**:
<span style="color:red">

 **Note**:

  * *Having the row of 4 buttons be at the bottom left corner. The name of button from left to right:*
   
      ***S1 - Reset Switch, S2 - Volume Down Switch, S3 - Recovery Switch, S4 - Power Switch***

</span>

      ![](/Image/1.png)

***
1. Power the TX2 and turn on Recovery Mode:
* Turn the TX2 on via Power Switch (4th button from the left)
* Hold Recovery Switch(3rd button from left) 
* Press Reset Switch(1st Switch from left). The light on the right of the Power Switch should turn off
* Release the Reset Switch. The light on the right of the Power Switch should turn back on
* Release the Recovery Switch. The light on the right of the Power Switch and Recovery Switch turn on.
   
   ![](/Image/2.png)

2. Connect host computer to Jetson TX2 through USB-Micro cable

<span style="color:red">

**Note:**

* *On the host computer, check if there has been a connection with the TX2 with command:* 
   ```
   $ lsusb
   ```
* *The TX2 should be shown as NVidia Corp.* 

</span>


### **Step 3: On the host computer**:
1. Open SDK Manger launcher using Ubuntu Launcher or open it from thett terminal with command: 

   ```
   $ sdkmanager
   ```
2. Login with NVIDIA account and follow the instruction
3. From the **Step 01 Development Environment** window, select the following:

   * From the **Product Category** panel, select the DRIVE development environment.

   * From the **Hardware Configuration** panel, select the host machine and target hardware.

   * From the **Target Operating System** panel, select the desired operating system, such as Linux or QNX. Notice that the target operating systems available may change, depending on the options that were selected in the other panels.

   * Finally, select any **Additional SDKs** that you wish to install.

   An ellipsis (...) in the bottom right corner of a category box indicates that more than one option is available. Click on the ellipsis to show a drop-down menu of available options.

   ![](/Image/3.png)

   Click **Continue** to proceed to the next step

4. From the **Step 02 Details and License**, you can expand the host components and target components panels to review the components that will be installed on your system.

* To review the licenses, click on the license agreements hyperlink at the bottom of the page.

* Enable the checkbox to accept the terms and conditions of the license agreements.

* If you want SDK Manager to download all setup files to a location other than the default path, expand the Download & Install Options drop-down menu, then select the path you wish to use.

   ![](/Image/4.png)

   Tick to **I acccept the term ....** and Select **Continue** to proceed to the next step

5. Before the installation begins, SDK Manager prompts you to enter your sudo password.
   
   ![](/Image/5.png)

* The display shows the progress of the download and installation of the software.
  
   ![](/Image/6.png)

* At the top, you can toggle between the Details and Terminal tabs. The Terminal tab shows detailed information about the download and installation, with any errors highlighted.
* On the Terminal tab, you can use the Filter text field to filter and search for specific information.
* A window will appear, asking for the username and password of the TX2. Leave in be and continue to the next step
   
   ![](/Image/7.png)


### **Step 4: On the TX2**:
1. Connect the TX2 to a monitor and setup the username/password.
   
   Follow all picture bellow:


### **Step 5: On the host computer**:
1. Enter the username/password you just set up.
   
   ![](/Image/7.png)
2. After the SDKManager has finished flashing, exit SDKManager

<span style="color:red">

**Note:**

* *After the SDKManager has finished flashing, some process of the host computer may fail. This is due to the host had already have the programs installed. Should it happens, just ignore it. As long as the target (TX2) is flashed, the process is considered success.*

* *If you have any other questions, please send me to the mail: manhlinh.nguyendinh@gmail.com*

</span>