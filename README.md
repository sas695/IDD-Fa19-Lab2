# Digital Timer
 
Include your responses to the bold questions below. Include snippets of code that explain what you did. Deliverables are due next Tuesday. Post your lab reports as README.md pages on your GitHub, and post a link to that on your main class hub page.

## Part A. Solder your LCD panel

**Take a picture of your soldered panel and add it here!**

![alt text](https://github.com/sas695/IDD-Fa19-Lab2/blob/master/Soldered%20LCD.jpg)

## Part B. Writing to the LCD
 
**a. What voltage level do you need to power your display?**
3.5V

**b. What voltage level do you need to power the display backlight?**
   5V
   
**c. What was one mistake you made when wiring up the display? How did you fix it?**

Initially I wired the LCD upside down. I reversed all the wires on the LCD side.

**d. What line of code do you need to change to make it flash your name instead of "Hello World"?**
 lcd.print("hello, world!");
**e. Include a copy of your Lowly Multimeter code in your lab write-up.**

const int rs = 12, en = 11, d4 = 5, d5 = 4, d6 = 3, d7 = 2;
LiquidCrystal lcd(rs, en, d4, d5, d6, d7);
int voltage = 0;
int analogPin = A0;

void setup() {
  // set up the LCD's number of columns and rows:
  lcd.begin(16, 2);
  // Print a message to the LCD.

}

void loop() {
  // set the cursor to column 0, line 1
  // (note: line 1 is the second row, since counting begins with 0):
  lcd.clear();
  voltage = analogRead(analogPin);
  // print the number of seconds since reset:
  lcd.setCursor(0,1);
  lcd.print(voltage);
  delay(100);
  
}

## Part C. Using a time-based digital sensor

**Upload a video of your working rotary encoder here.**

![alt text](https://github.com/sas695/IDD-Fa19-Lab2/blob/master/Encoder2.mov)

## Part D. Make your Arduino sing!

**a. How would you change the code to make the song play twice as fast?**
 
 You shorten the note Duration by dividing all the values by 2.
 
 int noteDurations[] = {
  10,10,10,2,2,10,10,10,2,4, \
  10,10,10,2,4,10,10,10,2,4};
  
  -->
  
   int noteDurations[] = {
  5,5,5,1,1,5,5,5,1,2, \
  5,5,5,1,2,5,5,5,1,2};
  
**b. What song is playing?**

Star Wars!

## Part E. Make your own timer

**a. Make a short video showing how your timer works, and what happens when time is up!**
 ![alt text](https://github.com/sas695/IDD-Fa19-Lab2/blob/master/Encoder2.mov)
**b. Post a link to the completed lab report your class hub GitHub repo.**
