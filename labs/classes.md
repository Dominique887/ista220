namespace Classes

{

    class Program

    {

        static void doWork()

        {

            Point origin = new Point();

            Point bottomRight = new Point(1366, 768);

            double distance = origin.DistanceTo(bottomRight);

            Console.WriteLine($"Distance is {distance}");

        }



        static void Main(string[] args)

        {

            try

            {

                doWork();

            }

            catch (Exception ex)

            {

                Console.WriteLine(ex.Message);

            }