ssh into the machine with this command:

ssh ctf-player@venus.picoctf.net -p 55507

Run ls command and looking at the output get the first part of the flag by reading the contents of the file via cat command.

Later, go to base directory using cd / command and retrive the second part of the flag via cat command.

Finally, go to home directory using cd ~ and retrive the third part of the flag via cat command. 

Concatenate all the parts and you will get the flag.