# GitflowOnWindows
This is a guide to install GitFlow on Windows

Please use a PowerShell or a CMD as Administrator to follow the above:

## Previous steps ##
Install Git for Windows https://git-scm.com/download/win

Next, Next, Next and choose your own options


## 1. Clone Gitflow
Clone the original repository for gitflow:
https://github.com/nvie/gitflow

```javascript
 git clone https://github.com/nvie/gitflow.git
```

## 2. Copy libiconv2.dll, libintl3.dll and getopt.exe to Git 
Copy **libiconv2.dll** and **libintl3.dll** and **getopt.exe** [from here](https://github.com/daniel553/GitflowOnWindows/tree/master/Files) inside **GIT** installation folder /bin
usually in: c:\Program Files\git\bin 

notice Windows x64 or x86 installation folder.

(Do not copy 'File' folder)

## 3. Installing gitflow

3.1 Go to the gitflow cloned repository

```javascript 
cd gitflow
```
3.2 Install shFlags submodule

```javascript 
git submodule init
```
you should get a message like:
> Submodule 'shFlags' (git://github.com/nvie/shFlags.git) registered for path 'shFlags'

3.3 Update submodule shFlags

```javascript 
git submodule update
```

3.4 Go to Contrib folder and install msysgit-install.cmd
```javascript 
cd contrib;
msysgit-install.cmd "C:\Program Files\Git"
```
please notice for Windows x64 or x86 installation folder

## 4. Check installation

if these steps were correctly followed the Git installation folder (/bin) must show the following files:
* git-flow-common
* git-flow-feature
* git-flow-hotfix
* git-flow-init
* git-flow-release
* git-flow-shflags
* git-flow-support
* git-flow-version

Now you can init a new Git Flow repository:
```javascript 
git flow init
```

## Tested on:
- Windows 8 x64
- Windows 8.1 x64
- Windows 10 x64

# Gitflow Official

https://github.com/nvie/gitflow
