first you need to download git
 "
https://git-scm.com/install
if you are on windows you need to add it manually to the environment variable to be recognized on your device 


2- then install conda add it to the sys path var 

after creativing venv using conda when trying to activate it for the first time you need firstly to initialize it usinig conda init powershell

then install wsl in powershell 
wsl --install 

in case not installed you need to do manual installation 
"""🛠️ The Fix: Manual WSL Installation
Step 1: Download the Kernel Update Package
First, download the WSL2 Linux kernel update package from Microsoft:
🔗 https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi

Run this .msi file after downloading.

Step 2: Download the Main WSL Installer
Go to the official Microsoft WSL releases page on GitHub:
🔗 https://github.com/microsoft/WSL/releases

Download the latest .msixbundle file (look for a file like wsl.2.x.x.x_x64.msixbundle, usually 400-500 MB).

Step 3: Install via PowerShell
Open PowerShell as Administrator (right-click Start menu → "Terminal (Admin)")

Navigate to your Downloads folder where you saved the .msixbundle file, or use its full path to run:

powershell
Add-AppxPackage -Path "C:\Users\ibrah\Downloads\wsl.2.x.x.x_x64.msixbundle"
(Replace the filename with the exact one you downloaded)

Step 4: Enable Required Windows Features
Still in PowerShell (Admin), run these commands one by one:

powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
Restart your computer after this step.

Step 5: Set WSL 2 as Default
After restarting, open PowerShell (Admin) again and run:

powershell
wsl --set-default-version 2"""

then it's better to use version 2 from the wsl 

wsl --set-default-version 2

then install ubuntu wsl --install ubuntu
and do the setup 
then we need to install miniconda into the ubuntu



wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
make sure to install it in the home directory not the app dir 
after installing and change the mod to be executable and run the file with setup to save all the configuration we need toupdate our shell statup (.bashrc) or (.profile)
run these lines 
~/miniconda3/bin/conda init bash
source ~/.bashrc
create new conda env here

optional setup your command line for better readability 
export PS1="\[\033[01;32m\]\u@\h:\w\n\[\033[00m\]\$ "




## Installation 

### Install the required packages

''' bash
$ pip install -r requirements.txt
'''

### Setup the environment variable 

''' bash
$ cp .env.example .env
'''

set your environment variable like "OPEN_AI_KEY" value











