# Remote Access Connection Tutorial
This tutorial will show you how to connect your terminal to remote server.

## VSCode
* To begin this tutorial we will first need to get Visual Studio Code. I did this by going to this website [here]( https://code.visualstudio.com/) and following the installation instructions.
* Once everything was downloaded, I opened it up and it looked like this.
![Image](https://cdn.discordapp.com/attachments/1063006870299758622/1063532251826106429/VSCode_Tutorial.png)
Keep in mind that when you open up VS Code, it may look slightly different from this screenshot.

## Remotely Connecting
Now that VS Code is installed, we will learn how to connect your terminal to a remote server in the case that you need to use a speciifc system or device.
* First, since I am using a Windows device, I needed to install [git](https://gitforwindows.org/) and made it so that your terminal uses git bash by default which you can find instructions to [here](https://stackoverflow.com/questions/42606837/how-do-i-use-bash-on-windows-from-the-visual-studio-code-integrated-terminal/50527994#50527994)
* Next, I opened up a new terminal by opening the "Terminal" tab at the top of VS Code and selected "New Terminal".  Then entered the command: 
```
$ ssh cs15lwiaua@ieng6.ucsd.edu
```
(Do not include the "$" in your terminal)
where "aua" are the letters that pertain to my course specific account which I found at [Account Lookup](https://sdacs.ucsd.edu/~icc/index.php)
Once I entered the command, this prompt showed up:
![Image](https://cdn.discordapp.com/attachments/1063006870299758622/1063220050061951038/image.png)

Next I just typed "yes" into the terminal and hit enter.


[How to reset your password](https://docs.google.com/document/d/1hs7CyQeh-MdUfM9uv99i8tqfneos6Y8bDU0uhn1wqho/edit)

It will then prompt you for your password, which will be the password that you just set your course account to.
Keep in mind that when you type your password, you won't be able to see anything being typed in the terminal. Just type in your password normally and once it works you should see a message like this:
![Image](https://cdn.discordapp.com/attachments/1063006870299758622/1063225400706220104/image.png)

If you entered the wrong password, another Password: prompt will appear in the terminal. If you enter the wrong password too many times, it will close the connection. You may need to wait a few more minutes for your password to update or you might want to try to reset your password again.

You may also get a message like this if you have failed the password check a few times but eventually log in:
![Image](https://cdn.discordapp.com/attachments/1063006870299758622/1063225963808309329/image.png)

Once you have successfully completed the steps up to this point, your terminal will be connected to the terminal of a computer in the CSE basement. This means that any command you run in the terminal, while connected remotely, will be ran as if it were done on the CSE basement computer.

## Trying Some Commands

Now that your terminal is connected, you can try running some commands







