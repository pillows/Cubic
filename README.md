sdfsdasdadasd# Cubic

[![](https://i.imgur.com/5tS5i3M.png)](https://cubic.vldr.org/)
f
---

A multiplayer WebGL voxel sandbox game written in C++, inspired by the classic version of Minecraft.

## Try it out

### Web
You can play the game from the web — [cubic.vldr.org](https://cubic.vldr.org/)

### Desktop

Alternatively, you can play the game by downloading the precompiled binaries for your platform:

- [Windows (x64)](https://github.com/vldr/Cubic/releases/download/Build/Cubic_Windows_x64.zip)  
[Windows (ARM64)](https://github.com/vldr/Cubic/releases/download/Build/Cubic_Windows_ARM64.zip)

  Download and unzip all files, then run the *Cubic.exe* executable.
  - You may need to install the latest [Visual C++ redistributable](https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist?view=msvc-170#latest-microsoft-visual-c-redistributable-version) for your platform.
- [MacOS](https://github.com/vldr/Cubic/releases/download/Build/Cubic_MacOS.zip)

  Download and unzip all files, then:
  * Move *Cubic.app* to the **Applications** folder.
  * Run the *Cubic.app* application.
  * Go to **Apple menu > System Settings > Privacy & Security** and allow *Cubic.app* to run.
- [Linux (Ubuntu/Debian)](https://github.com/vldr/Cubic/releases/download/Build/Cubic_Linux.zip)

  Download and unzip all files, then in a terminal, run:
  * `sudo apt update`
  * `sudo apt install libgl-dev libglew-dev libsdl2-dev`
  * `chmod +x cubic`
  * `./cubic`
- [Android](https://github.com/vldr/Cubic/releases/download/Build/Cubic_Android.zip)

  ownload and unzip all files, then install the *Cubic.apk* package:

## Controls

`W` and `S` to move forward and backward.   
`A` and `D` to move left and right.  
`V` toggles fly-mode.  
`E` or `B` opens the build menu.  

## Building

### Web

1. Open a terminal.
2. Install [Emscripten](https://emscripten.org/docs/getting_started/downloads.html) and [Make](https://www.gnu.org/software/make/manual/make.html).
3. Navigate to the `build/web/` directory.
4. Run `make -j`

After the build process completes, the output HTML, JS, and WASM files will be located in the `build/web/output/` directory.

### Windows

1. Install [Visual Studio](https://visualstudio.microsoft.com/#vs-section) with the "Desktop development with C++" component.
2. Open `build/windows/Cubic.sln` in Visual Studio.
3. If needed, upgrade the project's platform toolset to your Visual Studio's available platform toolset.
4. Select either **x64** or **ARM64** from the build architecture dropdown menu (top-center).
5. Select either **Debug** or **Release** from the build type dropdown menu (top-center).
6. Press **F7** or click **Build > Build Solution** to build the project.

After the build process completes, the output executable will be located either in `build/windows/x64/Debug` or `build/windows/x64/Release` for x64 debug/release builds, and `build/windows/ARM64/Debug` or `build/windows/ARM64/Release` for ARM64 debug/release builds.

### Linux

1. Open a terminal.
2. Install [clang](https://clang.llvm.org/) and [Make](https://www.gnu.org/software/make/manual/make.html).
* On Ubuntu/Debian, run `sudo apt install clang build-essential`
3. Install [SDL2](https://wiki.libsdl.org/SDL2/Installation#linuxunix) and [GLEW](https://glew.sourceforge.net/install.html) 
* On Ubuntu/Debian, run `sudo apt install libgl-dev libglew-dev libsdl2-dev`
4. Navigate to the `build/linux/` directory.
5. Run `make -j`

After the build process completes, the output executable will be located in the `build/linux/output/` directory.

### MacOS

1. Install [Xcode Command Line Tools](https://mac.install.guide/commandlinetools/4.html).
2. Open Terminal. 
3. Navigate to the `build/macos/` directory.
4. Run `make -j`

After the build process completes, the output executable will be located in the `build/macos/output/` directory.

### Android

1. Install [Android Studio](https://developer.android.com/studio).
2. Open the `build/android/` directory in Android Studio.
3. Click **Build > Generate Signed Bundle / APK** from the top menu.
4. Select **APK** and press **Next**.
5. For the **Key store path** entry, select the `debug.keystore` file located in the `build/android/` directory.
6. For the **Key store password** entry, enter `android`.
7. For the **Key alias** entry, enter `androiddebugkey`.
8. For the **Key password** entry, enter `android` and press **Next**.
9. Select either `release` or `debug` as the variant and press **Create**.

After the build process completes, the output executable will be located either in `build/android/app/debug/` or 
`build/android/app/release/` depending if you've selected a debug or release variant.

