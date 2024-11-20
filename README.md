# Wifi scanning using ESP32

## Overview
This project demonstrates a simple wifi scanning tool is a user-friendly application designed to detect, and display available WiFi networks.

This setup can be simulated using the [Wokwi Simulator](https://wokwi.com/projects/305569599398609473).

## Circuit Diagram

The circuit consists of three LEDs connected to the Arduino Uno through resistors. The LEDs turn on in sequence, creating the flip-flop effect.

![Circuit Diagram](https://github.com/Aruvi-B/wifi/blob/main/Images/circuit-diagram.png)

[**View the project on Wokwi**](https://wokwi.com/projects/305569599398609473)

### To download the entire project, including the circuit setup and code files:
Click **Download Project ZIP** from the top left corner on Wokwi.

---

## Steps to Build

### 1. Create a New GitHub Repository

- Go to [GitHub](https://github.com/) and create a new repository.
- Upload the following files:
  - `diagram.json`
  - `libraries.txt`
  - `wifi-scan.ino`
  - `wokwi-project.txt`

### 2. Set Up GitHub Codespaces

If you want to use GitHub Codespaces to build and simulate the project:

- Create a **new Codespace** from the repository's main branch.
- You will see the uploaded files in the GitHub explorer.

![Explorer](https://github.com/Aruvi-B/wifi/blob/main/Images/explorer.png)

### 3. Organize the Files

- Create a folder named `src` in your repository.
- Move the `wifi-scan.ino` file into this folder for better organization.

### 4. Add Necessary Configuration Files

In the root directory, add the following two configuration files for proper simulation.

#### `wokwi.toml` Configuration File

```
[wokwi]
version = 1
elf = ".pio/build/esp32/firmware.elf"
firmware = ".pio/build/esp32/firmware.bin"

# Forward HTTP requests from localhost to port 80 on the simulated ESP32
[[net.forward]]
from = "localhost:8180"
to = "target:80"
```

### `platformio.ini` Configuration File

```
; PlatformIO Project Configuration File
;
;   Build options: build flags, source filter
;   Upload options: custom upload port, speed and extra flags
;   Library options: dependencies, extra library storages
;   Advanced options: extra scripting
;
; Please visit documentation for the other options and examples
; https://docs.platformio.org/page/projectconf.html

[env:esp32]
platform = espressif32
framework = arduino
board = esp32dev
```
![Folder Constraints](https://github.com/Aruvi-B/wifi/blob/main/Images/explorer1.png  "Folder Constraints")

### 5. Install Necessary Extensions

Make sure the following extensions are installed in your Codespace or local environment:

1. **Wokwi Simulator** – To simulate your Arduino project.
2. **Arduino** – To handle Arduino code and libraries.
3. **C/C++** – For proper code syntax highlighting and IntelliSense.
4. **PlatformIO IDE** – To manage build configurations and dependencies.

![Extensions](https://github.com/Aruvi-B/wifi/blob/main/Images/extension.png?raw=true)

Once the extensions are installed, PlatformIO will begin configuring your environment. You may see a configuration loading message.

![PlatformIO Configuring](https://github.com/Aruvi-B/wifi/blob/main/Images/reload-platformio.png?raw=true)

### 6. Build the Project
Click the commit button to ensure the changes are confirmed.

![commit](https://github.com/Aruvi-B/wifi/blob/main/Images/commit.png?raw=true)

After PlatformIO finishes configuring, click **Build** to compile the code.

![PlatformIO Build](https://github.com/Aruvi-B/wifi/blob/main/Images/build.png?raw=true)

If everything is set up correctly, you should see a build success message.

![Build Output](https://github.com/Aruvi-B/wifi/blob/main/Images/build-output.png?raw=true)

### 7. Enter Your License Key

When prompted, enter your Wokwi license key to continue the simulation.
Once your Licence key is correct the below message showcased
![licence-key](https://github.com/Aruvi-B/wifi/blob/main/Images/licence-key.png?raw=true)

**Sample Reference Key:**
```
JnU9NDExNDMzOTE2NzAwNDgxNTM3Jm49QVJVVkkrQiZlPWFydXZpYmFsYW11cnVnYW4lNDBnbWFpbC5jb20meD0yMDI0MTIxOQDUGJjn9WS08KhQ1wqeo5hdL3e7YQBWpa2jQn5fFH5vC02cUWu561snpiR9XLkR_StBSXRv7j3DL34qMqmueEKSN3mG_P1QVlYK0UlhOScWEhgT1ZD3844r_S3IBcFKxAvg4fIbsX8388iPvgSCrBQNXzjxVS_Pk_PKUtc0eGsxY3pAfdNvl5MTMKuzIjneS8q3jYunrtkvMA30tCj_SZbCGj5eHJGlYkZ9IiSvAegqTkx2mBdDnhph0EyVVuYcITF9wEBAYKRQVisTNCtw_P8SSGZNcBZM4rCdeponWyQzYGzGu5_Sw3U51ZXB7_Sb0k7UAEncvYNuITgr85J_S2C3cwmG7r7z_SL

```

### 8. Start the Simulation

Once your license is verified, you can start the simulation. The LEDs should toggle in a flip-flop pattern as per your Arduino code.

![Start Simulation](https://github.com/Aruvi-B/wifi/blob/main/Images/start-simulation.png?raw=true)

Ensure that the Wokwi configuration paths in `wokwi.toml` are correct, and that all the peripherals, elf and firmwares paths are correctly defined.

![Ensure Correct Configuration](https://github.com/Aruvi-B/wifi/blob/main/Images/ensure.png?raw=true)

---

## OUTPUT

When the simulation starts, the board scan the wifi and print it in the terminal.

![Output](https://github.com/Aruvi-B/wifi/blob/main/Images/output.png?raw=true)

---

## Conclusion

- Congratulations! You have successfully built and simulated your **Wifi-Scanning**.
---
