We have limited version of the script. In order to access premium version, we must enter the licence key. Looking at the source code, we see that most part of the licence is revealed. We need to crack last 8 characters. The functions we are intersted in are ```enter_licence()``` and ```check_key()``` functions. 

In enter_licence() function, the program wants the user to enter a key and it strips the key into characters. Then, it passes it to check_key() function. If the line 134 evaluates true, we can access the premium version of the software and hopefully get the flag. 

Let's look at check_key function. It first compares the length of the inputted key to the length of the original key. 

The function must return True in order to get premium version of the software. Therefore, we need to validate every if statement. Each if statement checks current element with some character. We can look up these characters by running python interpreter. Do the following:
```
import hashlib
bUsername_trial = b"MORTON"
print(hashlib.sha256(bUsername_trial).hexdigest())
```
Above will reveal a hash. Looking at each index will give us current character. For example, ```print(hashlib.sha256(bUsername_trial).hexdigest()[4])``` will print one character which is the current character of the flag.

Since the if statement will return true, we move on to the next index and compare ```hashlib.sha256(bUsername_trial).hexdigest()[5]``` to current index. This goes for 8 characters and after you find this 8 characters replace it with ```key_part_dynamic1_trial``` variable. Then you will get the flag.
