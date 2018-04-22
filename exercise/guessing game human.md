using System;

using System.Collections.Generic;

using System.Linq;

using System.Text;

using System.Threading.Tasks;



namespace GuessingGame

{

  class Program

  {

    static void Main(string[] args)



    {



      Random r = new Random();



      int val = r.Next(1, 100);

      int guess = 0;

      bool correct = false;



      Console.WriteLine("I'm thinking of a number between 1 and 100.  Can you guess what it is?");



      while (!correct)

      {

        Console.Write("Guess: ");

        string input = Console.ReadLine();



        if (!int.TryParse(input, out guess))

        {

          Console.WriteLine("HA HA HA, That's not a number.");

          continue;

        }



        if (guess < val)

        {

          Console.WriteLine("Nope, the number I'm thinking is higher.  Guess again.");

        }

        else if (guess > val)

        {

          Console.WriteLine("No, the number I'm thinking is lower.  Guess again.");

        }

        else

        {

          correct = true;

          Console.WriteLine("You guessed it!  Good thing to, I was getting worried.");

        }

      }

    }

  }

}