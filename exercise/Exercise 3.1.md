## Exercise 2.1 


namespace Quadratic_equationd
{
    class Quadratic
    {
        static void Main(string[] args)


            //solve for x

        //identify the values of a b and c

        //insert the values of a b and c

        //solve for a b and c to find x

        

            {
            checked
            {
            darla();
                void darla()
                { 
                try
                {

                    Console.Write("Enter three value.:");
                        /* int a = int.Parse(Console.ReadLine());
                         if (a < 0)
                         {
                             Console.WriteLine("Use values greater than zero.");
                         }
                         else
                         {
                             jack();
                         }*/
                        jack();
                    void jack ()

                        {
                            int a = int.Parse(Console.ReadLine());

                            int b = int.Parse(Console.ReadLine());

                            int c = int.Parse(Console.ReadLine());
                            jane();

                            void jane()
                            {
                                Console.WriteLine($"The first value of x is {((-b - (Math.Sqrt(b * b) - 4 * (a * c))) / (2 * a))}");

                                Console.WriteLine($"The second value of x is {((-b + (Math.Sqrt(b * b) - 4 * (a * c))) / (2 * a))}");

                                Console.WriteLine("End of Program ");

                            }


                        }
                    }
                    catch (FormatException)
                    {
                        Console.WriteLine("enter numbers only");
                        darla();
                    }

                    catch (StackOverflowException)
                    {
                        Console.WriteLine("too large a value try again");
                        darla();
                    }

                    finally
                    {
                        Console.WriteLine("Program is Terminated");
                    }
                }






                





            }
        }
    }
    }
