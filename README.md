#  Using Jenkins With Private Github Repostory and Visual Studio


Download Lastest Version of Jenkins https://jenkins.io/download/thank-you-downloading-windows-installer-stable
for How to Install Jenkins on Windows https://dzone.com/articles/how-to-install-jenkins-on-windows

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

Download Lastest Version of Github Desktop https://central.github.com/deployments/desktop/desktop/latest/win32

Create Github private Repostory and include to Project .gitignore file from this link https://www.gitignore.io/api/csharp,windows,visualstudio


ssh-keygen -t rsa -b 4096 -C "mertguner"

$ ssh-keygen -t rsa -b 4096 -C "mertguner"
Generating public/private rsa key pair.
Enter file in which to save the key (/c/Users/Smit-Laptop/.ssh/id_rsa): [ENTER]
Created directory '/c/Users/Smit-Laptop/.ssh'.
Enter passphrase (empty for no passphrase): [ENTER]
Enter same passphrase again: [ENTER]
Your identification has been saved in /c/Users/Smit-Laptop/.ssh/id_rsa.
Your public key has been saved in /c/Users/Smit-Laptop/.ssh/id_rsa.pub.
The key fingerprint is:
SHA256:RHMgUrHsHxawnk9ywPl63AhSKGnHnM09h6baJx6VNlE mertguner
The key's randomart image is:
+---[RSA 4096]----+
|    ..=.+.E      |
|   + O O =       |
|  + * @ O .      |
| . o + B *       |
|    . B S        |
|     + & =       |
|    . = B .      |
|     . =         |
|      .          |
+----[SHA256]-----+

Goto C:\Users\Smit-Laptop\.ssh

id_rsa.pub file to https://github.com/settings/keys New SSH Key

id_rsa file to http://localhost:8080/credentials/store/system/domain/_/      Add Credentials
Kind = SSH Username with private key


relay forward --bucket github-jenkins http://localhost:8080/github-webhook/
