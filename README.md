Observations
Pyramid Level	Image Resolution	Detail Visibility	Computation
Level 0	High	Fine details visible	High
Level 1	Medium	Moderate details	Medium
Level 2	Low	Large structures only	Low
Level 3	Very Low	Very coarse features	Very Low

Algorithm
1.	Read the input image
2.	Convert the image from BGR to RGB format
3.	Display the original image (Pyramid Level 0)
4.	Apply pyrDown() to generate Level 1 of the pyramid
5.	Repeat downsampling to generate multiple pyramid levels
6.	Display all pyramid levels
7.	Observe image resolution changes and detail loss
8.	Apply edge detection on each pyramid level for comparison
