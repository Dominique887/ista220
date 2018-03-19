## C# exercise Try catch 


{ // Program to find the area and circumfrence of a circle
            double radius;
            double PI = 3.14159;
            double area, Cir, dia;
            enterthevalue();

            void enterthevalue()
            {
                try
                {


                    Console.WriteLine("Enter the Radius of a Circle ===> ");
                    radius = double.Parse(Console.ReadLine());
                    if (radius<0)
                    {
                        Console.WriteLine("Use value greater than 0");
                    
                    }
                      else
                     {
                        calculate();
                    }


                    void calculate()
                    {
                        area = PI * radius * radius;
                        Cir = 2 * PI * radius;
                        dia = 2 * PI;
                        userinput();

                        void userinput()
                        {
                            Console.WriteLine("The are of a circle is" + area);
                            Console.WriteLine("The circumference of a circle is" + Cir);
                            Console.WriteLine("The Diameter of a circle is" + dia);
                        }
                    }
                }
                catch (FormatException)
                {
                    Console.WriteLine("enter numbers only");
                    enterthevalue();
                }

                catch (StackOverflowException)
                {
                    Console.WriteLine("too large a value try again");
                    enterthevalue();
                }

                finally
                {
                    Console.WriteLine("Program is Terminated");
                }






            }
        }
    }
}