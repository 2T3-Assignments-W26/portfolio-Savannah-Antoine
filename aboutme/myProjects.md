# Gaming Project: Needles in a Haystack
This project was a word play on the famous expression of how finding something difficult is akin to:

> "Finding a needle in a haystack." 

 However, in the game's scenario finding one of these needles result in the main character "c" the "cowboy" in losing life. The goal of this game was for the charcter to collect as much money as possible to clear the game, else it would be gameover.

## Technologies Used 
* Programming Language: C#

### Main Instructions Screen
!["image"](..\aboutme\gamepic.png)
### Main GamePlay Screen
!["image"](..\aboutme\secondgamepic.png)
### Gameover Screen
!["image"](..\aboutme\gameoverscreen.png)

## Code Snippet

### First Code Example

```C#
 internal class Program
{

     static void Main(string[] args)
    {

         ShowSplashScreen();

         Console.BackgroundColor = ConsoleColor.DarkMagenta;
         Console.ForegroundColor = ConsoleColor.White;
         Console.CursorVisible = false;
         Console.Clear();

         ConsoleKey Key = ConsoleKey.NoName;//give the key no name to start, and will change as need progresses

         for (Num_Of_Money = 0; Num_Of_Money < Total_Num_Of_Money; Num_Of_Money++)
         {

             Money_PositionX[Num_Of_Money] = Random.Next(Console.WindowWidth);
             Money_PositionY[Num_Of_Money] = Random.Next(Console.WindowHeight);

         }
    }    
 }
```


### Second Code Example
```C#
Console.SetCursorPosition(0, 0);
Console.ForegroundColor = ConsoleColor.White;
Console.WriteLine();
Console.WriteLine(" HEALTH: " + Health);
Console.Write(" TOTAL MONEY: " + Total_Money);
Console.WriteLine();
Console.Write(" LEVEL: " + Level);

if (Total_Money == 50)//if points are 50 level up
{
    Health = 25;
    Level = 2;

}

Key = Get_Key_Stroke();//make function to process what key the user types in

if (Key == ConsoleKey.Spacebar)//menu will pop up when the user presses the spacebar and pause the game
{

    ShowSplashScreen();
    Console.BackgroundColor = ConsoleColor.DarkMagenta;
    Console.Clear();

}

Move(Key);//This function will process the movements made in the game

Obstacle_Move();
```

## Takeaway From Project Creation
Through the creation of this project I was able to gain hands on experience in using the programming c# to develop a functional gaming program. I learned more about the utilization of functions and how to ensure I'm using them optimally. Along with technical skills, I was also able to learn how much of an impact the UI can have on the gaming experience of the user.

# Gaming Project: Ultimate Jade Number Arcade
!["image"](..\aboutme\ArcadeGame.png)

For this game it's especially geared towards the mathematical minds out there, for those who enjoy playing with numbers, as this gaming project was designed with them in mind. The player first gets to access a main menu where they can choose to play any of 5 games. One of these games being the famous Collatz Conjecture problem. An interesting fact is that Collatz Conjecture is also known as the:

>"Hailstone Sequence or the Syracuse Problem"

## Technologies Used 
* Programming Language: C#

### Area of Rectangles 
!["image"](..\aboutme\Rectanglegame.png)


### Collatz Conjecture
!["image"](..\aboutme\Collatz.png)

### Hi Lo Game
!["image"](..\aboutme\HiLo.png)

## Code Snippets

### First Code Example
```C#
 static void OldestPerson()
 {
           bool success = true;
           string name, oldestname="";
           Int32 age,oldestage=0;

     //use boolean variable success to loop and stay in function
     //let user enter an age and number repeatedly by using loop
     //when name is end output the name and age of oldest
     //one name and age is always entered
           Console.WriteLine();
           Console.WriteLine(" Welcome to Option 4: the Oldest Person Program");
           Console.WriteLine(" Enter a name and age below to begin playing or type in the word 'end' to return to the main menu");
           Console.WriteLine();
     
            do
            {
        

                      Console.Write(" Please enter a name: ");
                      name = Console.ReadLine();
                      success = (name != "end");

                      if (success)
                      {

                                 Console.Write(" Please enter the age of " + name + ": ");
                                 age = getvalidnumber();


                      if (age > oldestage)
                      {

                                  oldestage = age;
                                  oldestname = name;

                      }
                      }
    
            } while (success);//end of do while loop

```
### Second Code Example

```C#
 do
 {

           Console.Write(" Please begin by entering a positive integer that's greater than the number 1: ");
           usernumber = getvalidnumber();
           lessorequalto1 = (usernumber < 1 || usernumber == 1);
           Console.WriteLine();
           Console.Write(" You entered the number: " + usernumber);
           Console.WriteLine();
           if (lessorequalto1)
           {

                     Console.WriteLine(" Try again! You need to enter a positive number that's greater than 1");
                     Console.WriteLine();


           }
 } while (lessorequalto1); 

do
{
          if (usernumber % 2 == 0)
          {

                     usernumber = usernumber / 2;
          }
         else
         {

                     usernumber = usernumber * 3 + 1;

         }

         if (usernumber > 100)
         {

                     timesover100++;

         }
         if (usernumber > 1 || usernumber < 100)
         {

                     timesbetween1and100++;

         }

          totaliterations = timesbetween1and100 + timesover100;

} while (usernumber != 1);
            
```
## Takeaway From Project Creation
Through dedicating time on enhancing the quality of the game, I learned how important the proper implementation of menus can be on the overall user experience. By allowing them to return to the menu once the game option they should has finished running it makes accessibility easier. Also adding an option for the user the quit the menu is greatly important if they no longer would like to continue playing.
