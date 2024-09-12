﻿# Neutron
Build apps with c# and web technologies using webview

# Prerequisite Windows
- Node js, install it from https://nodejs.org/en or use NVM (Node Version Manager) to easily install and manage nodejs versions https://github.com/coreybutler/nvm-windows
- Dotnet SDK, use the version you want to target, this framework support .Net 5, 6, 7, and 8 https://dotnet.microsoft.com/en-us/
- Enable Loopback, you need to enable the Loopback to make webview works on windows, run `CheckNetIsolation LoopbackExempt -a -n="Microsoft.win32webviewhost_cw5n1h2txyewy"` with elevated permission powershell, your user also need to do that, it's recommended to use an installer and add Loopback enabler to the installer script 

# Prerequisite Linux
- Node js, install it from https://nodejs.org/en or use NVM (Node Version Manager) to easily install and manage nodejs versions https://github.com/nvm-sh/nvm
- Dotnet SDK, use the version you want to target the framework support .Net 5, 6, 7, and 8 https://dotnet.microsoft.com/en-us/
- libwebkit2gtk, install using your distro package manager for debian use `sudo apt install libwebkit2gtk-4.0-37` and fedora use `sudo dnf install webkit2gtk4.0` if you distribute the app on linux the user of your app also need to install it

# Initializing The Project
Download the [neutroncli](https://github.com/annasajkh/Neutron/releases) 

for windows or linux

open the terminal and type
```neutroncli init```

fill out the option or you can pass it directly
```neutroncli init --name ProjectName --dotnet-version net8 --framework react_ts```

# Running The Project
cd to the project directory and type `neutroncli run`

or you can go to backend c# project directory and type `dotnet run`

# Building The Project
cd to the project directory and type 
```neutroncli build```

or pass it directly 
```neutroncli build --platform win_x64 --build-mode release --self-contained```

or you can go to the backend c# project directory and type
```dotnet publish --configuration Release --runtime win-x64 --self-contained```

it's decoupled from the neutroncli at this point so either way works