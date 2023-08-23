# axel-client
Axel's desktop client

# Setup

This section will walk through the set up process for Tauri, Typescript, React, and Framer Motion for development on Windows 10.

## 1. [Tauri](https://tauri.app/)

Tauri is a resource which brings Web Applications to Desktop with the help of Rust. Tauri does a great job documenting the [set up process](https://tauri.app/v1/guides/getting-started/prerequisites), but I will highlight the cruicial steps here to centralize set up.

**1. [Microsoft Visual Studio C++ Build Tools](https://visualstudio.microsoft.com/visual-cpp-build-tools/)**

Download and run Microsoft's Visual Studio Build Tools.

![image](https://github.com/Craftarc/axel-client/assets/92613118/84e510a4-6f65-44f6-955a-223009ac9685)

Select "Desktop development with C++" as shown above and ensure "MSVC . . . build tools" and "Windows 10 SDK" are included in the optional section, although in my experience my system preselected Windows 11 SDK and this was also viable. You may choose to keep the remaining preselected options or remove them, this is up to your preference. The minimal package size will be ~5GB so set up time for MVSC may be >15 minutes on your system.

**2. [WebView2](https://developer.microsoft.com/en-us/microsoft-edge/webview2/#download-section)**

Download the Evergreen Bootstrapper which will attempt to download a Runtime suited for your device architecture. Follow the prompts within the installer to finish setup for WebView2. Window machines with ARM architecture may run into issues with the Bootstrapper. If you find trouble with the Bootstrapper, try the Standalone Installer corresponding with your system. 

![image](https://github.com/Craftarc/axel-client/assets/92613118/09549610-92cc-45e8-b393-d9a0746cedd5)

Some Windows versions come with WebView2 Runtime preinstalled, notably Windows 11 systems, if this is the case you may skip this step.

**3. [Rust](https://www.rust-lang.org/tools/install)**

Download and run the Rustup-init.exe according to your system (32-bit or 64-bit).

<img width="977" alt="Screenshot 2023-08-23 at 2 18 02 PM" src="https://github.com/Craftarc/axel-client/assets/92613118/4c4d9ea9-b1e0-4cb9-b77a-7c48bf3e2c20">

Upon running the executable you'll be prompted with installation options. For our purposes the default installation works fine, select 1 and Enter.
After you see that Rust has been installed, press Enter or close out of your current command prompt session before utilizing Rust.

If you'd like to test see Tauri in action aside from Axel, you can follow Tauri's [Quick Start Guide](https://tauri.app/v1/guides/getting-started/setup/) for whichever available frontend stack you see fit. If you're unfamiliar with Web Development, I second Tauri's suggest to follow the guide for HTML/CSS/JS.
