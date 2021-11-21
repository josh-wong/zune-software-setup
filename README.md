# How to set up the Zune software and sync a Zune
This tutorial describes how to connect your Zune device to the Zune software and load apps and games onto it.

I created this tutorial because there are a few different resources online that provide these files but no exact instructions on how to:
- Install the Zune software
- Ensure your Zune device syncs with the software.
- Optional: Install the apps and games onto your Zune HD. 

I confirmed that the following instructions work on a Zune HD, and I assume it works the same on other Zune devices. However, the apps and games can be installed on only a Zune HD.

If you encounter any problems with these instructions or if the links no longer work, please feel free to open an issue with details or raise a pull request with your changes.

## Prerequisites
- [Notepad++](https://notepad-plus-plus.org/)
	- We will need to make admin changes to the "hosts" file in Windows. To do this, we will use Notepad++ since the default text editor in Windows may not allow you to make administrator-level changes.

## How to install the Zune software
1. Go to [Zune Update - RESOURCES](https://www.zuneupdate.com/resources/).[^1]
2. Click **ZUNE-SOFTWARE.ZIP**, and specify a folder to save the file to.
3. Go to the folder where you downloaded the software package, and double-click **ZunePackage.exe**.
> **Note:** User Account Control in Windows may prompt you with the message "**Do you want to allow this app to make changes to your device?**" If so, click **Yes**.
4. Click **Agree** if you accept the the terms of the Microsoft license terms.
5. Click **Install**. Installation will take about 1 minute.
6. After installation is complete, click **Close**. We don't need to open the Zune software at this point.

## How to connect the Zune with the Zune software
If you connect your Zune to your computer, your computer will not recognize the Zune. This is because Microsoft has decommissioned the server that facilitates communication between the Zune and the Zune software.

To force the software to recognize the device, we need to spoof the software into thinking the server is still available.
1. Open **File Explorer**, and go to **%SystemRoot%\System32\drivers\etc**.
2. Right-click **hosts**, click **Open with**, then select **Notepad++**.
3. At the bottom of the file, add the following to a new line: 

66.115.173.227	resources.zune.net

4. Save the file.

> **Note:** When saving the file, you may be prompted to launch Notepad++ in administrator mode since the "hosts" file is protected. If so, do the following:
>	1. Click **Yes** to open the file in administrator mode.
>	2. Click **Yes** when asked "Do you want to allow this app to make changes to your device?".
>	3. Save the file.

5. Plug in your Zune device to your computer to automatically install the device driver.
6. Open the Zune software. Your Zune device will then start syncing with the Zune software. 

> **Note:** If you previously reset your Zune to its factory default settings, you will see a different screen that shows your Zune has a "Required Update". If this screen appears, click **Accept**. Once this process is finished, you can begin syncing your media to your Zune HD.

To select which folders to sync with your Zune device, go to **Settings** in the Zune software. In **Collection**, you will see **Monitored folders** where you can choose which folders to sync.

## How to add apps and games to your Zune
I've only tested adding these apps and games onto a Zune HD. I don't know if these instructions will work to install the apps and games on non-Zune HD devices.
1. Go to **[Zune HD Apps.zip](https://www.dropbox.com/s/rqsifa8ukbkvybb/Zune%20HD%20Apps.zip?dl=0)** on Dropbox.[^2]
2. Click **Download**, and specify a folder to save the file to.
3. Go to the folder where you downloaded the ZIP file. Right-click **Zune HD Apps.zip** and click **Extract All**.
4. Follow the **Extract Compressed (Zipped) Folders** wizard to extract the files.
5. Go to **%LOCALAPPDATA%\Microsoft\Zune**. 
6. At the top of the **File Explorer** window, click **New** and select **Folder**. Then, name the new folder **Applications**.
7. In the folder that you extracted the apps and games to in Step 4, select which ones you want to add to your Zune. Then, move them into the **Applications** folder.
8. Connect your Zune device and open the Zune software. All the apps and games will automatically sync to your Zune.

> **Note:** Many of the apps, especially ones that require connecting to an external service like Facebook and Twitter, no longer work because those services' APIs have been changed. Most of the games should be playable though.

## References
Microsoft still hosts basic manuals for Zune and Zune HD devices. Please see [Zune Player and Zune HD Player Product Manuals](https://www.microsoft.com/en-us/download/details.aspx?id=30468) to download those manuals.

Donations in Bitcoin Cash (BCH) are greatly appreciated!

<img src="https://github.com/josh-wong/bitcoin-cash-node-on-raspberry-pi/blob/main/images/bitcoin_cash_qr_code_github_BCHN_tutorial.png?raw=true" style="zoom: 10%;" width="18%" height="18%" />

[^1]: Special thanks to [Zune Update](https://www.zuneupdate.com/) for providing an IP address that provides the server of reference that we need when connecting a Zune device with the Zune software.
[^2]: Special thanks to u/BenjaminGordonT on Reddit for providing a Dropbox link to the ZIP file of the Zune HD apps and games: [All the Original Zune HD Apps and Games!](https://www.reddit.com/r/Zune/comments/52yo3h/all_the_original_zune_hd_apps_and_games/)
