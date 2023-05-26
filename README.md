# Steganography
It is a program to carry out steganography (semagram-based steganography) to hide a secret message (image file) into a text-based file (word or rtf file).
# Working of the code:
- First we need to install pillow library to use Image related inbuilt functions
```
!pip install pillow
from PIL import Image
```
- Now as we know we are accounting for each pixel of image colour, I’ve used KMeans
clustering so that it can club neighbouring colours and form better clustering. This
improves the end image quality (The image formed when we zoom out the text).
(It should also be noted that our end image formed from text is bound to be fainter
than original image and hence this step helps give better result)
- I’ve also visualised this running the whole program without this step and it did result
in significantly better results.
- Now I’ve made a list of colours (i.e pixels). Now we have the pixels and dimensions
of the original image.
- Now I wanted to write the output text into a doc so I’ve used python docs library for it.
```
!pip install python-docx
from docx import Document
from docx.shared import RGBColor
```
- Now I’ve taken the text to be written as “10”, this same text will be used for all the
pixels to colour.
- Now I ran a loop from 0 to all of the colour pixels list. As I know from dimensions that
both length and width are 360 (for my input image). I’ve maintained a variable to
check the starting of a new line in the output file.
- I’ve also printed the line number to visualise the progress of the function. This way I
printed all the pixel colours with “10” as text.

# Test

The Original Image </br> 
![Knight](https://github.com/Aasrish/Steganography/assets/76608418/bb959fca-f530-4ef2-ac18-8d3a51e869f9)  

Output Text file on zooming out </br> 
![out2](https://github.com/Aasrish/Steganography/assets/76608418/2c186489-4a55-4b45-9065-3eb0809cd011)

Coloured letters in output text file </br> 
![Out3](https://github.com/Aasrish/Steganography/assets/76608418/7f7083a1-c85d-48d1-81b8-f84eb6a19412)

# Repo Contents

- This repository contains Steganograph_Program.ipynb, Steganograph_Pragram.py and Test.
- Steganograph_Program.ipynb is the source code file extracted from Google Colab.
- Steganograph_Program.py is the same source code file in .py format
- Test has an a test input image, and the output I got from the program.

# Note

- For the purpose of the task I’ve written the program in Python.
- As it's in python I found Google Colab to be very comfortable for the purpose. Hence I provided ipynb file.
- Since its google colab, we need to upload the image provided onto colab to run the code.
- I’ve written a code where we need not supply any input text file. It will automatically generate alternating 1 & 0 for the purpose of output file. The program includes the code to do the task.
- In order for the output image to be visible I had to change the font and between-line spacing in the output file manually.

# Team Members:

- Aasrish Vinay Perumalla (B20CS042)


