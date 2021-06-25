After looking into the C file, on line 93 we see a format string vulnerability. For more information check out the link: https://owasp.org/www-community/attacks/Format_string_attack

Let's use the payload %x.

After entering %x we get some hex values. Let's try it with 100 %x. Open python console and type this: print('%x' * 100). Copy the result and run the nc. Enter 1 and paste the copied text. Looking at the result, it might contain our flag. Copy the output and paste it to your prefered hex to ascii converter. The result seems gibberish except some meaningful text which is our flag. Although it is mixed up, it is our flag and we can convert it to the valid flag. Open python console and the following:

flag = 'ocip{FTC0l_I4_t5m_ll0m_y_y3n841645ebÿÜ'

for i in range(0, len(flag), 4):
	print(flag[i+3] + flag[i+2] + flag[i+1] + flag[i], end='')

That will reveal this: picoCTF{I_l05t_4ll_my_m0n3y_6148be54. We have to add closing curly brace which gives us the flag: picoCTF{I_l05t_4ll_my_m0n3y_6148be54}