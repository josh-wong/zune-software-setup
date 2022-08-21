# Connecting the Zune with the Zune software

After installing the Zune software, we need to add a registry setting in Windows and update the "hosts" file in Windows. This will ensure that your Zune can communicate with the Zune software without encountering errors or freezing.

## Add a registry setting to Windows

Since the Zune software was created and optimized for Windows 7, there seems to be an issue with Windows automatically adding the necessary registry settings. In this step, we will add a setting to the registry in Windows.

1. Go to **[Zune Update - TOOLS](https://www.zuneupdate.com/resources/tools/)**.
2. Click **ZUNE-APP-SETTINGS-REG-FILE.ZIP**, and specify a folder to save the file to.
3. Go to the folder where you downloaded the ZIP file to.
4. Right-click **ZUNE-APP-SETTINGS-REG-FILE.ZIP**, and select **Extract All**. In the wizard, click **Extract**. A registry file will be extracted.

   !!! warning

      If you're worried about the contents of the file and are comfortable checking what will be add to the Windows registry in the next step, you can open the file in Notepad++ to check its contents.

5. In the extracted folder, double-click **Zune Configure App Settings.reg**.

   !!! note

      If Windows prompts you about applying this registry setting, click **Run** to allow the file to be added to your registry.

6. When the warning appears, click **Yes**.
![Registry editor warning](https://github.com/josh-wong/zune-software-setup/blob/main/docs/assets/screenshots/registry_editor_warning.png?raw=true)

7. When the confirmation window appears, click **OK**.
![Registry editor confirmation](https://github.com/josh-wong/zune-software-setup/blob/main/docs/assets/screenshots/registry_editor_confirmation.png?raw=true)

## Update the "hosts" file in Windows

Since Microsoft decommissioned the server that facilitates communication between the Zune and the Zune software, we need to force the software to recognize the device. We do this by tricking the software into thinking the server is still available.

1. Open **File Explorer**.
2. Enter **%SystemRoot%\System32\drivers\etc** in the address bar, then click **Enter**.
3. Right-click **hosts**, click **Open with**, then select **Notepad++**.
4. At the bottom of the file, add the following to a new line: 
     `66.115.173.227	resources.zune.net`

4. Save the file.

   !!! note
      
      When saving the file, you may be prompted to launch Notepad++ in administrator mode since the "hosts" file is protected. If so, do the following:

      1. Click **Yes** to open the file in administrator mode.
      2. Click **Yes** when asked "Do you want to allow this app to make changes to your device?".
      3. Save the file.

5. If you have a PIN code set up on your Zune device, enter the code to unlock the device.
6. Plug in your Zune device to your computer to automatically install the device driver.
7. Open the Zune software.

   !!! note

      - If you previously reset your Zune to its factory default settings, you will see a different screen that shows your Zune has a "Required Update". If this screen appears, click **Accept**. Once this process is finished, you can begin syncing your media to your Zune HD.
      - If the music you have synced on your Zune device is stored on a cloud service (for example, OneDrive or Google Drive), you may see a window with the message "You haven't made a selection. Is this screen displayed correctly?" You can either wait until your music finishes downloading or you can cancel the files from being downloaded. After that, the Zune software will start from the initial setup screen.

8. If you want to apply the default settings to the Zune software, click **Start**. Or, if you want to change the default settings, click **Settings**, then follow the screens in the setup wizard.
![Zune software setup screen](https://github.com/josh-wong/zune-software-setup/blob/main/docs/assets/screenshots/zune_software_setup_screen.png?raw=true)

You've now finished installing the Zune software. If you have any music in the Zune software default folders or the folders that you chose in the setup wizard, those artists, albums, and songs will appear on the main screen.
![Zune software](https://github.com/josh-wong/zune-software-setup/blob/main/docs/assets/screenshots/zune_software.png?raw=true)

If you want to choose different folders to sync with your Zune device, go to **Settings** in the Zune software. In **Collection**, you will see **Windows Libraries** where you can choose which folders to sync.