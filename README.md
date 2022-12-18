# Image-Steganography

Steganography is the practice of concealing a file, message, image, or video within
another file, message, image, or video. Steganography is more discreet than
cryptography when we want to send secret information. On the other hand, the
hidden message is easier to extract.

# Understanding image steganography
Before diving into steganography, it is important to understand pixels and colour models. A pixel is the smallest building of an image and the colours in any pixel are (assume RGB) a function of the combination of proportions of red, green, and blue. So a pixel with a value of 0, 0, and 1 would mean 0 parts of red, 0 parts of green and 1 part of blue; in essence, this would turn out to be a blue pixel. In the case of an 8-bit system, a pixel can accommodate up to 8 digits (zeros or ones), and the largest number that could be represented in 8 digits is 11111111 which would be 255, and the smallest number that could be represented in 8 digits, would be 00000000 which would be 0. So any pixel in an 8-bit scenario could accommodate anything between 0 to 255 as a value for each of the colours. Now let’s say a random 8-bit grid has 3 pixels and each pixel having the below values for R, G, and B.


| |The proportion of Red (R)|	The proportion of Green (G)	|The proportion of Blue (B)|
|------------|--------------|--------------|----------|
|Pixel 1	|00101101	|00011100	|11011100|
|Pixel 2	|10100110	|11000100	|00001100|
|Pixel 3	|11010010	|10101101	|01100011|
And if we want to house a secret number 200, we get the binary value of that number, i.e, 11001000. and use each digit of that number to replace the least significant digit (mostly the last digit) of our pixel grid, indicated in bold red font. The new colour scheme would be as below: 


The proportion of Red (R)	The proportion of Green (G)	The proportion of Blue (B)
Pixel 1	00101101	00011101	11011100
Pixel 2	10100110	11000101	00001100
Pixel 3	11010010	10101100	01100011
This would alter colours in the original image in the three channels for the 3 pixels by the smallest amount, thereby rendering the alerted image almost indistinguishable from the original image.

# Result
Original image (Img.jpg) vs. Image after the message has been baked in (Img-enc.png) and their respective properties:
<p align="center">
  <img src="https://github.com/ritvic/Deepfake-Detection-Using-Reccurent-Neural-Network/blob/main/github_assets/System%20Architecture.png" />
</p>
<p align="center">
  <img src="https://github.com/ritvic/Deepfake-Detection-Using-Reccurent-Neural-Network/blob/main/github_assets/System%20Architecture.png" />
</p>


# Conclusion
Steganography is not intended to replace cryptography but rather to supplement it. If
a message is encrypted and hidden with a steganographic method it provides an
additional layer of protection and reduces the chance of the hidden message being
detected.
Steganography goes well beyond simply hiding text information in an image.
Steganography applies not only to digital images but to other media as well, such as
audio files, communication channels, and other text and binary files.


# Reference
https://www.mygreatlearning.com/blog/image-steganography-explained/

https://www.simplilearn.com/what-is-steganography-article
