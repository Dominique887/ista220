## Roulette exercise


## By:Dominique, Austin


namespace Roulette


{
    class Program
    
    
    {
        static void Main(string[] args)
        
        
        {
            Random rand = new Random();
            string numberResult = Spin(rand);
            string colorResult = ColorCheck(numberResult);

            Console.WriteLine("The wheel spins {0} - {1}", numberResult, colorResult);
        }
        public static string Spin(Random r)
        {
            int numberChosen = r.Next(0, 38);
            if (numberChosen == 37)
            {
                return "00";
            }
            else
            {
                return numberChosen.ToString();
            }
        }
        public static string ColorCheck(string result)
        {
            if (result == "0" || result == "00")
            {
                return "Green";
            }
            int number = Convert.ToInt32(result);

            if (number >= 1 && number <= 10 || number >= 19 && number <= 28)
            {
                if (number % 2 == 0)
                {
                    return "Black";
                }
                else
                {
                    return "Red";
                }
            }
            else
            {
                if (number % 2 == 0)
                {
                    return "Red";
                }
                else
                {
                    return "Black";
                }
