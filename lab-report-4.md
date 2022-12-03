# LAB REPORT 4 #

## PART 1 ##

### Our group chose: ###
*Changing the name of the start parameter and its uses to base.*
### The shortest sequence of vim commands to complete the task was: ###
/start\<enter>5sbase\<esc>n.n.n.:wq

Description:\
So we use "/" to get to the first instance where "start" is used.
![image](https://user-images.githubusercontent.com/114626503/205428405-01eddaf5-45a5-4de0-b8ae-10d35d39b211.png)\
Then we press enter to move to the first letter of the word.\
![image](https://user-images.githubusercontent.com/114626503/205428567-f5fc8a4a-da43-4656-a1ef-22c2d9a45184.png)\
Then we use the substitute command "s" by typing 5s so that it deletes all five letters of the word start. This command also puts us in insert mode.\
![image](https://user-images.githubusercontent.com/114626503/205428743-7b7043ff-c80d-45e4-86c7-8a71a3d48cc4.png)\
Now we just type "base" and the escape key to exit insert mode.\
![image](https://user-images.githubusercontent.com/114626503/205428792-ed67fc80-cabf-4076-8caf-00fbc9fe19f6.png)\
We have now made an edit and can use the n command to go to the next instance of "start" and then use . key to repeat the last change. \
![image](https://user-images.githubusercontent.com/114626503/205428856-14f1f339-751b-4754-9130-9ea2c49f968d.png)\
![image](https://user-images.githubusercontent.com/114626503/205428865-a95900fa-2441-4bbb-aae9-d1307fc7e442.png)\
![image](https://user-images.githubusercontent.com/114626503/205428876-91fedce2-ae50-4f1d-8df4-1cb03bd18237.png)\
After that we just type ":wq" to save and quit. w saves the changes and q exits vim.



## PART 2 ##
### Starting in visual studio code: ###
Took ~1 minute. Editing is pretty easy and fast, what takes the most time is having to scp to ssh and then logging into ssh and finally running, This took me especially more time because U still have to use a TA account because my own account's password is not working.

### Starting in ssh: ###
Took ~20 seconds. Since I am already logged into ssh all I have to to is use the editing commands I have learned to quickly edit the file. Then I can just run the file after saving and exiting from vim.

## QUESITON ##
If I had to work on a file remotely I would use VIM if I don't have to make too many edits. This is because the more edits in VIM I have to moke the more likely I will have some syntax error. It's prefferable because if you don't use vim you'll will have to edit the file locally then scp and log into ssh which would be time consuming and somewhat of a hassle. I'm okay with having to edit files locally when I have to make many edits because syntax errors are more likely to be caught and if there are any errors it will be hard to find.



