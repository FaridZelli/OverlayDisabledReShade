# Overlay Disabled ReShade
Here's how to disable the ReShade Startup Message / Splash Screen on (almost) any version.  
DISCLAIMER: This modification is only recommended for advanced users. Proceed at your own risk.  
And if you decide to use this build for a preset, remember to credit [***crosire***](https://github.com/crosire) and [***ReShade***](https://reshade.me)

# Method 1:  
I have already added a ready-to-use setup file, beware that it's extremely unstable and should ONLY be used for completed presets which you're not planning to adjust anytime soon. Hotkeys must be disabled. Download it [here](https://github.com/FaridZelli/OverlayDisabledReShade/raw/main/ReShade_Setup_OverlayDisabled_491.exe)

# Method 2 (DIY):  
In order to do it yourself, you will need:
1) Git
2) Visual Studio Community 2019 with C++, MSVS17 v141 Build Tools, .NET and Python modules installed
3) Notepad++

Step one:  
Head over to the official ReShade repository and clone everything, including the submodules  
https://github.com/crosire/reshade  
```
git clone --recurse-submodules https://github.com/crosire/reshade.git
cd reshade
git checkout 1dd52078131b18d633a03519b80a0a5041c7ae6d
git submodule update
```  

Step two:  
Go to the ```source``` folder and find ```runtime_gui.cpp```  

Step three:  
Open the file in Notepad++ and do a replace all  
Find what: ```show_splash = true```  
Replace with: ```show_splash = false```  
Save, check if it applied, close  

Step four:  
Follow the instructions at https://github.com/crosire/reshade#building to build the setup  
```
build [Release] (32bit)
build [Release] (64bit)
build [Release Setup] (64bit)
```
