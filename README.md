#  Using Jenkins With Private Github Repostory and Visual Studio

1. Download Latest Version of Jenkins [Download](https://jenkins.io/download/thank-you-downloading-windows-installer-stable)
[This Link](https://dzone.com/articles/how-to-install-jenkins-on-windows) for How to Install Jenkins on Windows 

## I used plugins for my project
* Email Extension Plugin
* Git client plugin
* Git plugin
* GitHub API Plugin
* GitHub Integration Plugin
* MSBuild Plugin
* Publish Over FTP
* change-assembly-version-plugin
* Text File Operations
* Locale plugin


2. Download Latest Version of Github Desktop [Download](https://central.github.com/deployments/desktop/desktop/latest/win32)

3. Create private Github Repostory

![](https://github.com/mertguner/Private-Github-Repostory-For-Jenkins/raw/master/Images/01.png)

4. Create a file named ignore.

![](https://github.com/mertguner/Private-Github-Repostory-For-Jenkins/raw/master/Images/02.png)
![](https://github.com/mertguner/Private-Github-Repostory-For-Jenkins/raw/master/Images/03.png)

5. Add all text to .gitignore file from this link https://www.gitignore.io/api/csharp,windows,visualstudio

![](https://github.com/mertguner/Private-Github-Repostory-For-Jenkins/raw/master/Images/04.png)
![](https://github.com/mertguner/Private-Github-Repostory-For-Jenkins/raw/master/Images/05.png)

6. Open C:\Program Files\Git\git-bash.exe 
- ssh-keygen -t rsa -b 4096 -C "{GitHub User Name}"
- and press enter 3 times

![](https://github.com/mertguner/Private-Github-Repostory-For-Jenkins/raw/master/Images/06.png)

7. Open to Folder C:\Users\%USERNAME%\.ssh

8. Create new Key in Github https://github.com/settings/keys 
- Click **New SSH Key**

![](https://github.com/mertguner/Private-Github-Repostory-For-Jenkins/raw/master/Images/07.png)

9. Open id_rsa.pub file with Text Editor.

![](https://github.com/mertguner/Private-Github-Repostory-For-Jenkins/raw/master/Images/08.png)
- Copy All text

10. Paste all text to KEY Area. Title must be Github username

![](https://github.com/mertguner/Private-Github-Repostory-For-Jenkins/raw/master/Images/09.png)

9. Open id_rsa file with Text Editor.

![](https://github.com/mertguner/Private-Github-Repostory-For-Jenkins/raw/master/Images/10.png)
- Copy All text

11. Open Jenkins > Credentials > System > Global credentials (unrestricted) [Shotcut Link for Localhost:8080](http://localhost:8080/credentials/store/system/domain/_/) 
Click **Add Credentials**

12. ![](https://github.com/mertguner/Private-Github-Repostory-For-Jenkins/raw/master/Images/11.png)
- Select "SSH Username with private key" to Kind
- Check Enter directly 
- Username is "{GitHub User Name}"
- Past all text to Key Area

13. Get ssh Link of private repository

![](https://github.com/mertguner/Private-Github-Repostory-For-Jenkins/raw/master/Images/12.png)

14. Create New Jenkins Item
- Change Source Code Management

![](https://github.com/mertguner/Private-Github-Repostory-For-Jenkins/raw/master/Images/Connect.gif)
