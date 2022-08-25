# Polycom VXX-401/411
**![PolyVVX-401_Phone (Insert Pic Here)](https://github.com/KI5CYA/wiki/blob/main/PolyVVX-401_Phone.png)**


The Polycom VXX-401/411 Phone Series are 12-line IP Phones with Color Display, which is a full-featured VoIP (Voice over Internet Protocol) phone that provide voice communication over an IP network. It provides traditional features, such as call forwarding, redialing, speed dialing, transferring calls, conference calling, and accessing voice mail. Calls can be made or received with a handset, headset, or speaker.

The Polycom VXX-401/411 Series IP Phones provides a web interface (aka: GUI - Graphical User Interface) for the phone user that allows you to configure some features of your phone by using a web browser.

This article will guide you through the steps for basic configuration to make it work with HOIP.

**Note:** These steps MIGHT work with other Polycom Models. The examples below are to give guidance in your attempts to provision/configure your Polycom Models.

## Step 1
**Get the IP address of your phone**

a. Press the **"Home"** Button Icon on your Polycom Phone.

**![PolyVVX-401_Phone_Home_Button (Insert Pic Here)](https://github.com/KI5CYA/wiki/blob/main/PolyVVX-401_Phone_Home_Button.PNG)**

b. On the **"Display Screen"** and using the **"Arrow Keys"** to scroll and select **"Settings"**.
c. Scroll down to **"Status"** and hit **"Select"**.
d. Scroll down to **"Network"** and hit **"Select"**.
e. Scroll down to **"TCP/IP Parameters"** and hit **"Select"**.

You should have a number which is similar to your Intranet address of  192.168.xxx.xxx

## Factory Reset - (if required)
The below steps are an option to be considered, if one the following is observed:

* The phone is on a boot loop and no longer going to the home menu
* The default password or mac password doesn't work
* If it's a 3rd party phone

1). Reboot the phone and wait for the starting application.
2). While the phone is in the starting application wait for the cancel button to appear then press it.
3). The phone will show a 7 seconds count down. This is the only open window to press the key combination to go to the hard reset page.
* **VVX series (VVX300, 301, 310, 311, etc)**: Press and hold 1 3 5 within the 7-second count down until it prompts you to the password page
* **Sound Point IP 335**: Press and hold 1 3 5 7 within the 7-second count down until it prompts you to the password page
* **Sound Point IP series (IP550,560,570, etc)**: Press and hold 4 6 8 and '*' within the 7-second count down until it prompts you to the password page
* **Conference Phone IP5000, 6000, 7000**: Press and hold 1 3 5 7 within the 7-second count down until it prompts you to the password page

4). Enter the device's MAC ID as the password (e.g 0004f28619dc).
5). Press the 2nd soft key that corresponds to the mode or (encoding) to change it to A->abc or a->abc.
6). Then (for example) to select the letter F, press the 3 key three times.
                                                                             


## Step 2

**Logging in to the Phone Web User Interface**
* 1). On your PC, open a Web browser window. (Note: Your PC must be on the same subnetwork as the phone.)
* 2). Enter the IP address in the browser address bar.

You will now see this screen (see picture):

**![PolyVVX-401_Phone_Admin_Login (Insert Pic Here)](https://github.com/KI5CYA/wiki/blob/main/PolyVVX-4xx_Admin_Login.png)**




## Step 3 - Configure "Simple Setup" Fields
After successful login of User ADMIN, click on  **"Simple Setup"** button near the top left side of the screen.
Then you will population the only the **"Header Fields"**  as the pictured in the below example.

**![PolyVVX-4xx_Simple_Setup - (Insert Picture Here)](https://github.com/KI5CYA/wiki/blob/main/PolyVVX-4xx_Simple_Setup.png)**

As the example pictured above, enter your information into the following fields:

**TIME SYNCHRONIZATION**
**Alternate SNTP Server**: north-america.pool.ntp.org
**Alternate Time Zone**: (Your GMT Zone)

**SIP SERVER**
**Address**: pbx-us1.hamsoverip.com
**Port**: 5160

**SIP OUTBOUND PROXY**
**Address**: pbx-us1.hamsoverip.com
**Port**: 5160

**SIP LINE IDENTIFICATION**
**Display Name**: How you want your "Caller ID" to be displayed to the Called Party
**Address**: Enter your New Six Digit Extension/Phone number
**Authentication User ID**: Enter your New Sex Dight Extension/Phone number
**Authentication Password**: Enter your password provided to you from HOIP
**Label**:  Your choice on how you want to label your "Line Key" on your phone display

Select **"SAVE"** before leaving screen.  
If phone reboots, log back in as user ADMIN and continue to Step 4

## Step 4 - Configure "SIP" Fields
After completing Step 3, click on  **"Settings"** button near the top left side of the screen and choose **"SIP"**
Then you will population the only the **"SIP Fields"**  as the pictured in the below example.

**![PolyVVX-4xx_SIP_Settings_Setup - (Insert Picture Here)](https://github.com/KI5CYA/wiki/blob/main/PolyVVX-4xx_SIP_Settings.png)**

As the example pictured above, enter your information into the following fields:

**OUTBOUND PROXY**
**Address**: pbx-us1.hamsoverip.com
**Port**: 5160
**Transport**: TCPpreferred

**SERVER 1**
**Special Interop**: Standard
**Address**: pbx-us1.hamsoverip.com
**Port**: 5160
**Transport**: TCPpreferred
**Expires (s)**: 3600
**Subscription Expires (s)**: 3600
**Register (Radio Button)**: <YES>
**Retry Timeout (ms)**: 0
**Retry Maximum Count**: 3
**Line Seize Timeout (s)**: 30

Select **"SAVE"** before leaving screen.  
If phone reboots, log back in as user ADMIN and continue to Step 5

## Step 5 - Configure "LINE" Field
After completing Step 4, click on  **"Settings"** button near the top left side of the screen and then choose **"LINES"** and highlight **Line 1**.
Then you will population the only the **"Line 1"**  as the pictured in the below example.

**![PolyVVX-4xx_Line_Settings - (Insert Picture Here)](https://github.com/KI5CYA/wiki/blob/main/PolyVVX-4xx_Line_Settings.png)**

As the example pictured above, enter your information into the following fields:


**IDENTIFICATION**
**Display Name**: Your choice.  (This is the name YOU will see on your Phone Display for Line 1)
**Address**: Your New Six Digit Extension/Phone number
**Label**: Your choice. Recommend using the same entry from **"Display Name"** above.
**Type (Radio Button)**: <Private>
**Third Party Name**: <Leave Blank>
**Number of Line Keys**: 1
**Calls Per Line**: Default is "24" - Enter at least "1"
**Enable SRTP (Radio Button)**: <Yes>
**Offer SRTP (Radio Button)**: <No>
**Require SRTP (Radio Button)**: <No>
**Server Auto Discovery**: <Enable>

**AUTHENTICATION**
**Use Login Credentials (Radio Button)**: <Disable>
**Domain**: pbx-us1.hamsoverip.com
**User ID**: Your New Six Digit Extension/Phone number
**Password**: Your password provided to you from HOIP
** *Author Note**:  I left the fields populate, as I recall that the data-fill being required.*


**OUTBOUND PROXY**
**Address**: pbx-us1.hamsoverip.com
**Port**: 5160
**Transport**: DNSnaptr

**SERVER 1**
**Special Interop**: Standard
**Address**: pbx-us1.hamsoverip.com 
**Port**: 5160
**Transport**: DNSnaptr
**Expires (s)**: 3600
**Subscription Expires (s)**: 3600
**Register (Radio Button)**: <YES>
**Retry Timeout (ms)**: 0
**Retry Maximum Count**: 3
**Line Seize Timeout (s)**: 30

Select **"SAVE"** before leaving screen.  
Now with Steps 3 thru 5 provisioned/configured, reboot the phone to bind the changes/additions.

Written by Mark KI5CYA
Last Updated: 08/25/2022