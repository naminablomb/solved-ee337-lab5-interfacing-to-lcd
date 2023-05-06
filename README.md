Download Link: https://assignmentchef.com/product/solved-ee337-lab5-interfacing-to-lcd
<br>
In this set of experiments, we develop display and other utilities which will be useful to us for the later experiments. For these experiments, you will have to attach the LCD unit to the Pt-51 board. Remember that the display has to be plugged in such a way that it extends <em>outside </em>the board and <em>not </em>over it. Plugging in the display in the wrong orientation may damage it ! Refer to the attached tutorial on Liquid Crystal Display Control.

For this lab, you are provided with a subroutine (lcd.asm) which writes characters to the LCD. Study the program to see how it works.

<strong>Note: </strong>For doing these exercises you can make use of bin2ascii, readNibble, packNibble and delay subroutines, developed in an earlier lab, to display ascii characters on the LCD.

<strong>1 LabWork</strong>

<ol>

 <li>Understand the working of given asm code.</li>

 <li>Using the supplied routine for writing characters to the LCD, write a program that willdisplay <strong>Your Roll Number </strong>on the first line and your name on the second line. Pad the display lines with spaces such that these are centered on the LCD when displayed. Your name should not be hard coded in the program, but stored as array of characters in the upper RAM. The program should display whatever is stored in this array.[5 points]</li>

</ol>

1

<ol start="3">

 <li>Write a program that will display the contents of 8051 registers on the LCD in thefollowing format:</li>

</ol>

First line of display should show the values of registers A, B and PSW in the format: “ABPSW = ?? ?? ??”. The second line should display the contents of R0, R1 and R2 in the format “R012 = ?? ?? ??”. Here ?? represents the content of those registers in Hex. This display should be held for about 5 seconds.

After this, the display should show “R345 = ?? ?? ??” for contents of R3, R4 and R5 on the first line and “R67SP = ?? ?? ??” on the second line for contents of R6, R7 and Stack Pointer.

<ol start="4">

 <li>Write a program that will display an address and its contents. The address will bespecified by setting switches on the board and you can use the readNibble First nibble provides the MSB of the address and second nibble the LSB of the address.</li>

</ol>

The address location should be displayed in the first line in the format: “Location: ??”. The contents of the specified memory location should be displayed in the second line in the format: “Contents: ??”. Here ?? represents the address and its contents in the two lines respectively.

The following sequence should repeat continuously. That is, read MSB, wait for 5 seconds, read LSB, wait for 5 seconds, display the memory location and its contents as mentioned, wait for 5 seconds, read the switches again