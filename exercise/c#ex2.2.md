using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Console_app5
{
    class Program
    {
        public static object grade { get; private set; }

        static void Main(string[] args)
        {
            Console.WriteLine("sum ten numbers ");
            int sum = 0;
            int count = 0;
            int avg = 0;
            _get_sum();




            Console.WriteLine("The sum is " + sum);
            Console.WriteLine("The average is: {0} ", sum / 10);
           

            void _get_sum()
            {
                count++;
                Console.WriteLine("Enter integer" + count + ":");
                sum += int.Parse(Console.ReadLine());

                if (count < 10)
                {


                    _get_sum();


                }
                else
                    return;
            }



            {
                avg = (sum / (count - 1));
                if (avg < 60)
                {

                    Console.Write("Your grade is  F");
                }
                else if ((avg >= 60) && (avg < 70))
                {

                    Console.Write("Your grade is  D");

                }
                else if ((avg >= 70) && (avg < 80))
                {

                    Console.WriteLine("Your grade is  C");

                }
                else if ((avg >= 80) && (avg < 90))
                {

                    Console.WriteLine("Your grade is  B");

                }
                else if ((avg >= 90))
                {

                    Console.WriteLine("Your grade is A" );
                }
            }
        }
    }
}
            
