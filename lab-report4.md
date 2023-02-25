## Setup
# 1. Delete existing repository
To delete the exisiting forked repository first go to the repository page labeled "lab7" then click settings:
![image](https://user-images.githubusercontent.com/122576325/221054502-b2005fe0-af34-47a0-8537-072c066c9576.png)

Next, you want to scroll all the way to the bottom of the page, then under "Danger Zone", click "Delete this repository"
![image](https://user-images.githubusercontent.com/122576325/221054607-df95a823-9d13-428e-aa6a-ff3786a0e83b.png)

Then, just type in the message it prompted to confirm you want to delete the repository, then click 
on the button that says "I understand the consequences, delete this repository"
![image](https://user-images.githubusercontent.com/122576325/221055019-db492111-3b03-4990-89dc-44c9f5f22a51.png)


# 2. Create new repository
Next you want to fork your repository again, go to the repository you want to fork
then in the top right side of the screen click "Fork" and click "Create Fork"
![image](https://user-images.githubusercontent.com/122576325/221055211-2b5b248a-e810-4dbf-953c-5a28cc038824.png)
![image](https://user-images.githubusercontent.com/122576325/221055369-723492da-89c5-44eb-aa77-60b7f9767e82.png)

## The Real Deal

# 3. Start the timer
Started the timer on my phone.

# 4. Log into ieng6
Keys Pressed: ```<ctrl-c>,<right-click>,<enter>```

In my local terminal I copy and pasted my login information from a separate document by highlighting the text, then using
```<ctrl-c>``` to copy and ```<right-click>``` to paste in the terminal and hit <enter> to execute the command.
```
ssh cs15lwi23aua@ieng6.ucsd.edu
```
and it logged me in without having to type a password

![image](https://user-images.githubusercontent.com/122576325/221056459-8bd39638-ff27-4a3c-80e1-c1763e032b62.png)

# 5. Clone the fork of the repository
Keys Pressed: ```<ctrl-c>,<right-click>,<enter>```

To clone the fork in my repository, I copy and pasted the command 
```
git clone git@github.com:vluu03/lab7.git
```
in a similar fashion to the way I copy and pasted the ssh login
  
![image](https://user-images.githubusercontent.com/122576325/221057318-3a6fdef2-52db-416a-bdd9-04a8eed2d4a2.png)

I got the url from the forked github repository page found here:
  
![image](https://user-images.githubusercontent.com/122576325/221056914-83dc7e31-1cd0-41a0-b7fb-d07581fa4a39.png)
 

# 6. Running the tests
Keys Pressed: ```cd l, <tab>, <enter>, <ctrl-c>, <right-click>, <enter>, <ctrl-c>, <right-click>, <enter>```

To run the JUnit tests of the forked repository, I first changed into the directory of the repository by typing
  ```
  cd l
  ```
  then I hit ```<tab>``` to auto complete to ```lab7``` then ```<enter>```
 
 Next, I compiled the JUnits tests by copy and pasting in the terminal
 ```
 javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java
 ```
 I used ```<ctrl-c>``` to copy the command and ```<right-click>``` in the terminal
 to paste the command in
 
 I ran these tests by copy and pasting in the terminal
 ```
 java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests
 ```
 in the same way as the previous command. And it showed one of the tests failing.
 
 ![image](https://user-images.githubusercontent.com/122576325/221313251-32d841b0-d894-4164-94d8-c415cab1f4ca.png)
 
 # 7. Editing the code
 Keys Pressed: ```nano L, <tab>, .j, <tab>, <enter>, <ctrl-v>, <down> x10, <right> x12, <backspace>, 2, <ctrl-o>, <enter>, <ctrl-x>, javac L, <tab>, ., <tab>, <enter>```
 
To edit and fix the bug in the code, I first typed in
```
nano L
```
then I hit ```<Tab>``` to auto complete it to ```nano ListExamples```, and from there I just put in a ".j" to the end to where it was ```nano ListExamples.j``` and hit ```<Tab>``` again to auto complete it to ```nano ListExamples.java```, then I hit ```<Enter>``` and it takes me to a page like this:
![image](https://user-images.githubusercontent.com/122576325/221317384-bda6c4fb-cb09-48aa-a8c4-b506473ba130.png)

From here, I pressed ```ctrl - v``` to take me to the next page, then I held ```<Down>``` until I reached the line of code that says ```index1 += 1;``` within the ```while(index2 < list2.size())``` loop, which you could also reach if you press ```<Down>``` 10 times.
Next, I held ```<Right>``` until the white box was directly to the right of the "1" in ```index1```, which you could also reach by pressing ```<Right>``` 12 times.
After that, I pressed ```<backspace>``` then ```2```.
This should replace ```index1``` with ```index2```, making the line of code ```index2 += 1;```, which fixes the bug since the proper index is now getting incremented, meaning there is no more infinite loop.

![image](https://user-images.githubusercontent.com/122576325/221319235-1f11202d-3996-4590-b289-2f62e6728f87.png)

Finally, I save and exit out of the code by pressing:
```<ctrl-o>``` ```<enter>``` then ```ctrl-x```
I then compiled the file by typing in ```javac L``` then ```<tab>``` to auto complete it to ```javac ListExamples```, then I added in a "." then hit ```<tab>``` to make it complete to ```javac ListExamples.java``` and pressed <enter> to execute the command.

# 8. Running the tests again
Keys Pressed: ```<up>, <up>, <enter>```

To run the tests again, I just pressed ```<Up> <Up> <enter>```

![image](https://user-images.githubusercontent.com/122576325/221320587-f9d66cd2-115a-4741-a3d1-73c31bbfbb8e.png)

# 9. Commiting and pushing the changes
Keys Pressed: ```git add L, <tab>, .j, <tab>, <enter>, git commit -m "/", <enter>, git push origin main, <enter>```

To push the changes to the github repository, I first typed 
```git add L``` then ```<tab>``` then added in ".j" and ```<tab>``` to auto complete to 
```git add ListExamples.java``` then pressed ```<enter>```

Next, I typed ```git commit -m "/"``` then ```<enter>```
I used "/" as the commit message since it was the closest to the " key.

Finally, I typed ```git push origin main``` and pressed ```<enter>```

![image](https://user-images.githubusercontent.com/122576325/221320884-0b76f42d-45af-4fc5-910d-8a6b39c1c050.png)

and when I look back to the lab7 repository, I can see the updated message showing it pushed successfully

![image](https://user-images.githubusercontent.com/122576325/221321561-7e702299-5806-4643-ac08-52fc12b688b6.png)




 


  
  





