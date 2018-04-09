







C# exercise by Dominique,Austin 
# The Sum of an Array




## static void Main(string[] args)
        {
            try
            {
                int[] A = new int[] { 0, 2, 4, 6, 8, 10 };
                int[] B = new int[] { 1, 3, 5, 7, 9 };
                int[] C = new int[] { 3, 1, 4, 1, 5, 9, 2, 6, 5, 3, 5, 9 };
                int avg = 0;
                A.Sum();
                avg = (A.Sum() / A.Length);
                for (int i = 0; i < A.Length; i++)
                {                   
                    Console.WriteLine($"The sum is: {A.Sum()}");
                    Console.WriteLine($"The average is: {avg}");
                    return;
                }
            }
            catch (ArgumentOutOfRangeException)
            {
               
            }
