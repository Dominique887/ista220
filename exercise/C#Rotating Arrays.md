## Rotating Array

By: Dominique, Austin

## static void Main(string[] args)
        {
            int[] A = new int[] { 0, 2, 4, 6, 8, 10 };

            int[] B = new int[] { 1, 3, 5, 7, 9 };

            int[] C = new int[] { 3, 1, 4, 1, 5, 9, 2, 6, 5, 3, 5, 9 };

            
            Console.WriteLine("\nArray1: [{0}]", string.Join(", ", B));

            int temp = B[0];

            for (int i = 0; i < B.Length - 1; i++)
            {
                B[i] = B[i + 1];
            }
            B[B.Length + 1] = temp;
            Console.WriteLine("\nAfter rotating array becomes: [{0}]", string.Join(", ", B));
        }
    }
}