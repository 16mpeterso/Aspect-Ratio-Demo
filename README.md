# Aspect-Ratio-Demo
This demonstrates how you can make any content (images, videos, etc) with a preset aspect ratio fill an element with a different aspect ratio by using hidden overflow and a little math.

To run the Demo just open index.html in a web browser.
NOTE: The HTML refrences Google's JQUERY upload so you do need internet for this to run properly.

It has been tested and does work on Google Chrome and Firefox.

You can also note the javascript is pretty sketchy and there are like 0 comments, I appologize for this.
If I see community intrest in this project I may update it with better and more comments and addded features like the following:
*A url input field allowing you to refrence your own image/ maybe video
*An input field to change the aspect ratio of the image 
*Being able to click on and edit the image margin, and the element width and height and have changes displayed 



The math:

In case #1 the image has a 4:1 Aspect Ratio and the element has a 6:4 Aspect Ratio:

Image:
OOOOOOOOOOOOOOOO
OOOOOOOOOOOOOOOO
OOOOOOOOOOOOOOOO
OOOOOOOOOOOOOOOO

Container element:
     ||||||
     ||||||
     ||||||
     ||||||

Container Element with visable overflow:
OOOOO||||||OOOOO
OOOOO||||||OOOOO
OOOOO||||||OOOOO
OOOOO||||||OOOOO

Container Element with hidden overflow:
    OOOOOO
    OOOOOO
    OOOOOO
    OOOOOO

Element width: 6 
Element Height: 4
Image Width: Element Height * (image aspect ratio:4/1) = 4*(4/1) = 16
Image Height: Element Height = 4
Image margin-left: (Image Width - Element Width) / -2 = (16-6) / -2 = -5 





In case #2 the image has a 4:1 Aspect Ratio and the element has a 1:8 Aspect Ratio:

Image:
OOOOOOOOOOOOOOOO
OOOOOOOOOOOOOOOO
OOOOOOOOOOOOOOOO
OOOOOOOOOOOOOOOO

Container Element:
||||||||||||||||
||||||||||||||||

Container Element with visable overflow:
OOOOOOOOOOOOOOOO
||||||||||||||||
||||||||||||||||
OOOOOOOOOOOOOOOOO

Container Element with hidden overflow:
OOOOOOOOOOOOOOOO
OOOOOOOOOOOOOOOO

Element width: 16 
Element Height: 2
Image Width: Element Width = 16
Image Height: Element width / (image aspect ratio:4/1) = 16/(4/1) = 4
Image margin-top: (Image Height - Element Height) / -2 = (4-2) / -2 = -1 
