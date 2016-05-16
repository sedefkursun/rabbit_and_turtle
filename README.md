# rabbit_and_turtle
write with C.

INTRODUCTION 

     
      Used Libraries 

1) stdio.h library	: This library is used for using basic functions.
2) windows.h library : In this library contains the sleep function so we use this library. 
3) time.h library : There is time function in this library. If we want to use time function, we use this library.
4) stdlib.h library : This library is used for using rand function.

The Purpose of The Program

Rabbit & Turtle characters race on an racecourse. Each characters step count is calculated randomly by the program for each turn. All the race and race result show on the screen end of the race. 

The Rules of The Program

Rules of rabbit :
1) Rabbit's steps can be between 1 and 6.
2) Rabbit can moves forward only 1,2,3 and 6 random numbers.
3) If the random number is 4, rabbit must go back 4 step.
4) If the random number is 5, rabbit must wait 2 tour.

      Rules of turtle :
1) Turtle's steps can be between 1 and 3.
2) Turtle can moves forward only 1,2 and 3 random numbers.


      Global Variables In This Program

      Global variables : These variables are used by all functions in the program. Before we begin  to  write program, we define these variables. When we define these variables ,  the first letter must big, next letters are small according to camel case that is rule of code writing.

      Constants : If parameter value remain unchanged, which is defined to constant. These  parameters must write with big letters.

RACE_LENGTH : This variable means length of the racecourse length. And the variable is equal to 78.
turtlePossition :The location of the turtle. This variable is initially zero.
rabbitPossition : The location of the rabbit. This variable is initially zero.
rabbitSleepTime :This variable means rabbit jail steps. This variable is initially zero because rabbit has not jail in the beginning.
raceFinished  : This variable is control variable of the race is finish or not.
RABBIT  : R symbol is used for rabbit.
TURTLE : T symbol  is used for turtle.


THE MAİN FUNCTİON

All programs are begin to work in main function. Initially, main function is executed by the program. If there is not main function, program does not work. What do we want from this program? We want to draw a scene. We want to watch  the turtle and the rabbit race then print on screen result. To make them ; firstly, we must write a function for draw the scene but the contents of this function will write after the main function. I gave its name drawScreen. Now, only we must take into variables on the scene  this function. Then I use Sleep function for wait the image on the screen. Sleep function is special function. This function inside windows.h library. Secondly, we decide to use loop. We think For loop. We need to we know how many times repeat race in order to use  For loop. When the number of cycles are not certain, used to While loop or Do While loop. Because if case suitable condition, loop is continues. I prefer to use Do while loop. we accept  each turn of the a tour in loop, that we must calculate turtle and rabbit possition. Therefore, we must write new two functions. One of them is calculated rabbit possition, other  is calculated turtle possition. And  their possitions write into these functions. Next step, we must again print scene on screen because their possitions changed.
We use Sleep functions again. And We finish the loop identify the condition. In my cycle, condition is raceFinished equal to zero. Thirdly, We use If loop in order to write result.
Hence, I write this condition. If rabbit possition equal than greater seventy-eight, the program writes RABBIT WINS!! Else the program writes TURTLE WINS!! The main function finished in here.

The drawScreen Function

When we started this function, we must know writing some parameters in function. These parameters are turtlePossition, rabbitPossition and RACE_LENGTH. First of all, we write a new value in function. This value name counter for me. This value is equal zero because this value using in For loops. Then we clear to screen with system(‘cls’) function. Why ? For a more clearer image. Then, Is it greater than zero, so we check. If it is greater than zero, the program print “Rabbit 1. or  2. sleep time :)”. This about rabbitSleepTime equal how much. Secondly, we draw scene. How do we draw? We can start a line for way. Thus, we write counter equal RACE_LENGHT  from counter equal zero and the counter will increase one by one in For loop. Print dash on screen. Next, we write rabbit position. Therefore, we write same For loop but after For loop , we write if loop. If  rabbitPossition is  equal counter, the program print “R” but if which is not equal counter , the program print space on screen. Again we write For loop but then we write if loop. This loop condition is if counter mod three is equal zero, the program print dash on screen. But if counter mod three is not equal zero, the program print space on screen. Following we write turtle position same rabbit position. And first For loop is written. In this way, this function is finish.

The RabbithowmuchStep Function

This function is written by us. What does this function do? This function generate rabbit's step count by randomly for each calling.Thus, we use srand function. And we use into srand function time function each time for  different results. Then new value is written. I gave its name randomNumber. We take to randomNumber is mod six then add one because rabbit is move six step. So that. This function is finish.



The TurtlehowmuchStep Function

This function is written by us. And this function similar to the RabbithowmuchStep Function
This function generate turtle's step count by randomly for each calling. Hence, we use srand function. And we use into srand function time function each time for  different results. Then new value is written. I gave its name randomNumber. We take to randomNumber is mod three because turtle is move three step. In this way, This function is finish.

The rabbitPossitionFunction 

Primarily, two new values are defined by us. One of them is stepNumber, other is thenPossition. After, we write a While loop. This loop’s condition is rabbitSleepTime greater than zero. If condition is true, rabbit wait the tour and rabbitSleepTime is one reduced. Then, stepNumber is equated RabbithowmuchStep function. Next to, Swich loop is written. stepNumber is written in Swich loop. If stepNumber is equal four, thenpossition is equal to atPossition  reduced four step. So rabbit back to four step. Or if stepNumber is equal five, rabbit possition is not change. RabbitSleepTime is assigned two and thenpossition is equal to atpossition. If stepnumber is not four or five, thenpossition is equal atpossition add stepnumber. Finally, we write two if loops. First if loop’s condition is thenpossition smaller than zero, thenpossition is equated zero. Second if loop’s condition is thenpossition equal then greater  seventy-eight thenpossition is equated seventy-eight and raceFinished is assigned one.
This function is finish in here.

The turtlePossitionFunction

First of all, two new values are defined. One of them is thenpossition, other is stepnumber. Then, stepnumber is equated TurtlehowmuchStep function. thenpossition is equal atpossition add stepnumber. Lastly, if loop is written. This loop’s condition  is thenpossition equal then greater  seventy-eight thenpossition is equated seventy-eight and raceFinished is equated one. And program is finish with this function.



