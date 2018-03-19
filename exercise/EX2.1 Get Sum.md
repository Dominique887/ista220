--headers on
--echo on


Author: Dominique,Austin
Date: mar 04,2018






  Console.WriteLine("sum ten numbers");
            int sum = 0;
            int count = 0;
            _get_sum();
            
            
            
            Console.WriteLine("The sum is" + sum);

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
        }
    }
}
