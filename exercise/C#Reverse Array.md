## Reverse Array
## By:Dominique, Austin






##  static void Main(string[] args)
        {
            int[] A = new int[] { 0, 2, 4, 6, 8, 10 };
            
            // Creates and initializes a new array
            Array Imawsome = Array.CreateInstance(typeof(String), 5); 
            int[] C = new int[] { 3, 1, 4, 1, 5, 9, 2, 6, 5, 3, 5, 9 };
            Imawsome.SetValue("Yea!!", 0);
            Imawsome.SetValue("Renlist", 1);
            Imawsome.SetValue("Didn't", 2);
            Imawsome.SetValue("I", 3);
            Imawsome.SetValue("Glad", 4);
            
             // Displays the values of the Array.

            Console.WriteLine(value: $"The Imawsome has the following values: {Imawsome}");
            PrintIndexAndValues(Imawsome);
            
            // Reverses the sort of the values of the Array.
           
           Array.Reverse(Imawsome);
            
            // Displays the values of the Array.

            Console.WriteLine("After Reversing:");
            PrintIndexAndValues(Imawsome);
        }
       
       //This gives the output
       public static void PrintIndexAndValues(Array Imawsome)
        {
            for (int i = Imawsome.GetLowerBound(0); i <= Imawsome.GetUpperBound(0); i++)
                Console.WriteLine("\t[{0}]:\t{1}", i, Imawsome.GetValue(i));
        }
    }
}

