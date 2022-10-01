FINDING 15L SSH ACCOUNT & RESETTING PASSWORD
  Go to https://sdacs.ucsd.edu/~icc/index.php and from there sign in and reset the 15L account password
  
  **For my lab I was able to reset my password but everytime I am prompted in the terminal to log in the 
    password never works and when I went to reset my account passowrd again with the same password that I 
    chose it said I cannot reuse the previous password which confirms that I am ussing the correct password 
    it's just not working. :(

INSTALLING VISUAL STUDIO CODE
  Go to https://code.visualstudio.com/ and install visual stUdio code from there.

CONNECTING TO SSH REMOTELY
  Use the following command in the terminal to connect to the ssh:
  ssh <account username>@ieng6.ucsd.edu

  Confirm that you want to connect by typing:
  yes

  Then enter your account password

RUNNING COMMANDS IN SSH
  Now that you are logged into the ssh try some commands to see if they work in the ssh.
  Some commands you can try:
  cd ~
  cd
  ls
  ls -lat

MOVING FILES FROM PERSONAL CLIENT TO SSH VIA SCP
  Create a java file on your personal computer and save it.
  Then go to that directory in your terminal and run the following command:
  scp WhereAmI.java <account username>@ieng6.ucsd.edu:~/

  Log in using the password you set and now the file should be in yor ssh. You can check by logging into the ssh 
  and using the 'ls' command.

SETTING AN SSH KEY
  On your client to set an ssh key type in the following command:
  ssh-keygen
  
  Then hit enter again when the file save prompt shows up so that it is set to the default path.
  
  If you are on windows follow the ssh-add steps on:
  https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_keymanagement#user-key-generation
  
  Now copy the public key to the '.ssh' directory to your ssh account.
  
  Log into your ssh and use the following command to create the '.ssh' directory:
  mkdir .ssh
  
  Then logout and move the 'id_rsa.pub' to your ssh account with the following command:
  scp <id_rsa.pub file path> <account username>@ieng6.ucsd.edu:~/.ssh/authorized_keys
  
HOW TO SAVE TIME IN REMOTE RUNNING
  Adding a command in quotes after the ssh login command will runn the command as so as you are logged into 
  ssh:
  ssh <account username>@ieng6.ucsd.edu "<command>"
  
  You can also run multiple commands at once by separating them with semicolons.
  
  You can also save time using the up arrow on your keyboard to get the last command that was run in case you 
  need it.
    
End of lab report.


