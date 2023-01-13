# Remote Access Connection Tutorial
This tutorial will show you how to connect your terminal to remote server.

## VSCode
To begin this tutorial we will first need to get Visual Studio Code. To do this you go to this website [here]( https://code.visualstudio.com/) and follow the installation instructions.
Once everything is downloaded, open it up and it should look something like this.
![Image](https://cdn.discordapp.com/attachments/1063006870299758622/1063220050061951038/image.png)
Keep in mind that when you open up VS Code, it may look slightly different from this screenshot.

## Remotely Connecting
Now that VS Code is installed, we will learn how to connect your terminal to a remote server in the case that you need to use a speciifc system or device.
First, if you are on a Windows device, you will need to install [git](https://gitforwindows.org/) and make it so that your terminal uses git bash by default which you can find instructions to [here](https://stackoverflow.com/questions/42606837/how-do-i-use-bash-on-windows-from-the-visual-studio-code-integrated-terminal/50527994#50527994)
Next, we will start using ssh to connect to the remote server.
First, you want to open up a new terminal by either using the hotkey (Ctrl/Command + `) or you can open the "Terminal" tab at the top of VS Code and select "New Terminal". 
In your new terminal, enter the command
```
$ssh cs15lwi___@ieng6.ucsd.edu
```
where the blank between "wi" and "@" is filled in with the letters that pertain to your course specific account which you can find in the [Account Lookup](https://sdacs.ucsd.edu/~icc/index.php)
For this course, you will need to reset your password (even if you already have one) in order to connect your terminal to the remote terminal. 
[How to reset your password](https://docs.google.com/document/d/1hs7CyQeh-MdUfM9uv99i8tqfneos6Y8bDU0uhn1wqho/edit)
Once the password is reset, you will likely have to wait a few minutes for it to update.






