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
*Programming Language: C#
