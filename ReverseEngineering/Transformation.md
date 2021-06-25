To get to know more about unicode refer to this link: https://stackoverflow.com/questions/2241348/what-is-unicode-utf-8-utf-16

Open up Python interpreter and do the following:

flag = "灩捯䍔䙻ㄶ形楴獟楮獴㌴摟潦弸弰摤捤㤷慽"

print(flag.encode("utf-16-be"))

You may ask, why utf-16-be instead of utf-16? The truth is I do not know either. After trying utf-16, looked up different utf-16 types and it turns out there is 3 of them. UTF-16, UTF-16-BE and UTF-16-LE. I tried utf-16-be and the flag is revealed.
