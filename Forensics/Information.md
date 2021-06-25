First of all, let's look at metadata of the image using exitfool.

exiftool cat.jpg

When examining the output, licence seems odd. It seems like a base64 text. Go to https://gchq.github.io/CyberChef/ and convert it to text by giving a recipe for from base64. The output gives us the flag.