# Lab Report 4 #

## 1. Delete any existing forks of the repository you have on your account ##
* I first navigated to "Your repositories" and entered the "lab7" repository to delete it

![image](https://user-images.githubusercontent.com/122580604/221070513-d16e29e2-0343-4526-a52a-729be02198b0.png)

* I then clicked on the "Settings" tab and scrolled all the way down to press "Delete this repository"

![image](https://user-images.githubusercontent.com/122580604/221070574-ea7013a6-45b9-440c-b795-5451fbcf4f7f.png)

![image](https://user-images.githubusercontent.com/122580604/221070438-ae25a528-f855-4f8f-96b5-93214bff7717.png)

## 2. Fork the repository ##
* I made a fork of https://github.com/ucsd-cse15l-w23/lab7

![image](https://user-images.githubusercontent.com/122580604/221070785-417fc140-0414-4fb5-b40e-510268132cfa.png)

## 3. Start the timer! ##
* I pressed start on Google's stopwatch feature

![image](https://user-images.githubusercontent.com/122580604/221070997-54f694c9-ca7e-4276-9489-78e70e9bef1f.png)

## 4. Log into ieng6 ##
* I open the bash terminal in Visual Studio Code and typed `ssh cs15lwi23ahy@ieng6.ucsd.edu` and did not need my password to sign in due to making an SSH key beforehand for my device to be recognized for logins

![image](https://user-images.githubusercontent.com/122580604/221071472-ec5f0f3b-9fa4-4a17-8df1-21553aed0255.png)

## 5. Clone your fork of the repository from your Github account ##
* On the forked repository of my GitHub account, I went to the green "<> Code" button and clicked SSH and then copied the GitHub SSH link to my clipboard

![image](https://user-images.githubusercontent.com/122580604/221071945-d8e09caf-75e2-4c47-b639-006317367aad.png)

* I went back to my bash terminal and typed `git clone git@github.com:vinniethecaptain/lab7.git` and pressed enter to clone the repository onto the remote computer

## 6. Run the tests, demonstrating that they fail ##
* I type `cd lab7` to make "lab7" my working directory
* I copied and pasted this line into my terminal to compile the tester and the program `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java`
* I copied and pasted this line into my terminal to run the tester `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests` and it showed a failure

![image](https://user-images.githubusercontent.com/122580604/221079225-b5bbcc0f-b384-48ad-9bac-f25d3b72f1a4.png)

## 7. Edit the code file to fix the failing test ##
* I typed and enter `nano ListExamples.java` to edit the code from the bash terminal

![image](https://user-images.githubusercontent.com/122580604/221079621-9887e772-e026-48d2-bc72-990abc165395.png)

* In the shortcut `<ctrl> + <w>` (called where is), which is used to quickly move your cursor to the beginning of a phrase you input, I typed "while(index2" and hit enter to move my cursor there

![image](https://user-images.githubusercontent.com/122580604/221081562-0e34d999-c5b0-4b09-aea2-7e8b0c87f7a2.png)


* I pressed `<down> <down>` `<right> <right> <right> <right> <right> <right> <right> <right>` to place my cursor where the error was and then hit `<backspace>` to change `index1` to `index2`
* I then pressed `<ctrl> + <o>` and then `<enter>` to save my edits
* I used `<ctrl> + <x>` to exit nano 

## 8. Run the tests, demonstrating that they now succeed ##
* I recompiled and reran the programs like I did in step 6 and when I did, there were no more failures

![image](https://user-images.githubusercontent.com/122580604/221081624-fb87fef5-f507-4891-8856-e3390422dda5.png)

## 9. Commit and push the resulting change to your Github account ##
* I typed `git add ListExamples.java` to the changes for git commit
* Then I typed `git commit -m "fixed runtime error"` to commit the change and to notate what I had fixed
* Finally, I used `git push` to push my changed onto my GitHub repository

![image](https://user-images.githubusercontent.com/122580604/221082046-088e4b79-bfb8-4aa9-a307-d85e0599a646.png)

![image](https://user-images.githubusercontent.com/122580604/221082076-12e5e8c3-dfe1-479c-b716-5f3bfb6018f4.png)




