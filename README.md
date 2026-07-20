# WearOS-Watch-Faces
Built my own custom Wear OS terminal watch face because I refused to pay a dollar for it. Free, open-source, and step-by-step setup guide included!
# PREVIEW
<img width="480" height="480" alt="Screenshot_20260720_134310_One UI Watch Home" src="https://github.com/user-attachments/assets/aebc4343-d2ba-4675-9c5b-3b6da8f609fd" />

💬 Support

Running into an issue? Message me on Reddit: u/LuciiEditzz

**#Watch Face on my watch at the end **

## 📑 Prerequisites & Project Downloads

Before you begin, you will need the official designer environment and the raw layout file from this repository:

1. **Official Software:** Download and install [Samsung Watch Face Studio](https://developer.samsung.com/watch-face-studio/download.html) (Available for Windows and macOS 11+).
2. **Project Configuration File:** **[Download the Raw WFS Project File](./Terminal%20Watch%20Face.wfs)**
3. **Terminal Typography:** Download and install the [JetBrains Mono Font](https://www.jetbrains.com/lp/mono/) (Click "Download Font" and install the Regular/Bold `.ttf` files to your computer). *Note: If you skip this, the text alignment and terminal look will break.*

> **Mac Users Note:** When installing Watch Face Studio, if macOS blocks the package saying the developer cannot be verified, open your Mac's **System Settings > Privacy & Security**, scroll down to the bottom, and click **Open Anyway**.

## 📂 Step 1: Open the Project
1. Launch **Watch Face Studio** on your computer.
2. Click **Open Project**, navigate to your downloads folder, and select the downloaded `Terminal Watch Face.wfs` file.
3. The complete, pre-configured terminal environment will boot up on your canvas with all accurate custom formatting, text tags, and colors intact.

## 🛜 Step 2: Enable Wireless Debugging on Your Watch
To sync the project from your computer to your wrist, both devices must be connected to the **exact same Wi-Fi network**.

1. On your watch, swipe down and go to **Settings > System > About watch > Software info**.
2. Tap **Software version** (Samsung watches) or **Build Number** (Pixel Watches) repeatedly 7 times until a popup notification says *"Developer mode turned on"*.
3. Back out to the main **Settings** page and tap the newly unlocked **Developer Options** row at the bottom.
4. Scroll down and turn **ON** both **ADB Debugging** and **Wireless Debugging**.

## 💻 Step 3: Terminal Pairing Handshake
Because modern Wear OS versions require a secure pairing handshake before allowing external tools to sync, Watch Face Studio's interface can sometimes time out. We will bypass this instantly using your computer's terminal.

### Mac

1. Open the **Terminal** app on your Mac.
2. Run this command to map Watch Face Studio's background connection tools to your system terminal path:
   ```bash
   export PATH=$PATH:/Applications/WatchFaceStudio.app/Contents/tools/mac
   ```
3. On your watch, under the Wireless Debugging menu, tap **Pair new device**. Leave this screen open! It will display a unique 5-digit pairing port and a 6-digit pairing code.
4. In your Mac Terminal, enter the pairing command using your watch's IP address:
   ```bash
   adb pair YOUR_IP_ADDRESS:YOUR_PORT
   ```
   then enter the pairing code when prompted.

   **Example:**
   ```
   adb pair 192.168.68.100:39039
   Enter pairing code: 585764
   Successfully paired to 192.168.68.100:39039
   ```

### Windows

Follow along with this video guide: [YouTube Tutorial](https://www.youtube.com/watch?v=sF3us77rbdc) (2:44–3:54 covers the command prompt workflow).

1. Download the official [Google ADB Platform Tools for Windows](https://dl.google.com/android/repository/platform-tools-latest-windows.zip).
2. Extract the downloaded `.zip` file to a folder on your computer.
3. Open your Windows Command Prompt (CMD), type `cd` followed by the exact path to your extracted `platform-tools` folder, and press Enter.
4. On your watch, tap **Pair new device** under Wireless Debugging.
5. In your Windows Command Prompt, run:
   ```
   adb pair 192.168.68.100:YOUR_PORT
   ```
6. Type in the 6-digit pairing code shown on your watch when prompted and press Enter.

The watch should now be paired. If you run into any issues, refer to the [video guide](https://www.youtube.com/watch?v=sF3us77rbdc).

## 🚀 Step 4: Flash and Run on Device (Inside Watch Face Studio)
Once your terminal says `Successfully connected`, head back into the Watch Face Studio application to push it to your wrist:

1. **Locate the Run Button:** Look at the top right corner of the Watch Face Studio window and click the **Run on Device** icon (it looks like a small smartwatch with a play arrow).
2. **Scan for Your Watch:** In the popup window that appears, click the **Scan** button.
3. **Select Your Device:** Your watch will appear in the available devices list as an active IP address (matching your watch's Wi-Fi network). Click on your watch from the list.
4. **Launch:** Watch Face Studio will compile the project layout, build the background files, and push them straight onto your watch screen. The retro terminal face will pop up natively on your wrist in a matter of seconds!

NOTE : If the allignment comes slightly crooked, move the top most group accordingly, message me on reddit for support 

On My watch : 
<img width="3024" height="4032" alt="IMG_0162" src="https://github.com/user-attachments/assets/1fb84847-6706-4ffb-bf21-36ea49430d8b" />
<img width="3024" height="4032" alt="IMG_0159" src="https://github.com/user-attachments/assets/b9f70690-f60c-4a50-862a-8873e58d2348" />
<img width="4284" height="5712" alt="IMG_0158" src="https://github.com/user-attachments/assets/bb2e3c7e-917e-427a-a6e5-8338e1fb412d" />


