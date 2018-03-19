namespace Farm_Animals
{
    class Program
    {
        static void Main(string[] args)
        {
            try
            {
                pig Porkypig = new pig("th-th-th-that's all folks", "bacon", "red bowtie", 5);

                Porkypig.Speak();
                Porkypig.Eat();
                Porkypig.Clothes();
                Porkypig.Age();

                bird Tweetybird = new bird("tawt i saw a puddy tat", "chicken", "blue dress", 6);

                Tweetybird.Speak();
                Tweetybird.Eat();
                Tweetybird.Clothes();
                Tweetybird.Age();

                bunny Bugsbunny = new bunny("eh what's up doc", "carrot", "pink dress", 7);

                Bugsbunny.Speak();
                Bugsbunny.Eat();
                Bugsbunny.Clothes();
                Bugsbunny.Age();

                Duck Daffyduck = new Duck("desthpicable", "steak", "black suit", 9);

                Daffyduck.Speak();
                Daffyduck.Eat();
                Daffyduck.Clothes();
                Daffyduck.Age();
            }
            catch (FormatException fex)
            {
                Console.WriteLine(fex.Message);
            }

            catch (Exception ex)
            {
                Console.WriteLine(ex.Message);
            }
        }



        public class pig
        {
            private string speak;
            private string eat;
            private string clothes;
            private int age;

            public pig(string pigspeak, string pigeat, string pigclothes, int pigage)
            {
                speak = pigspeak;
                eat = pigeat;
                clothes = pigclothes;
                age = pigage;
            }

            public void Speak()
            {
                Console.WriteLine("porkypig say {0}", speak);
                Console.ReadKey();
            }

            public void Eat()
            {
                Console.WriteLine("porkypig eats {0}", eat);
                Console.ReadKey();

            }
            public void Clothes()
            {
                Console.WriteLine("porkypig wears {0}", clothes);
                Console.ReadKey();
            }
            public void Age()
            {
                Console.WriteLine($" porkypig's age is {age}");
                Console.ReadKey();
            }
        }

        public class bird
        {
            private string speak;
            private string eat;
            private string clothes;
            private int age;

            public bird(string birdspeak, string birdeat, string birdclothes, int birdage)
            {
                speak = birdspeak;
                eat = birdeat;
                clothes = birdclothes;
                age = birdage;
            }

            public void Speak()
            {
                Console.WriteLine("tweetybird say {0}", speak);
                Console.ReadKey();
            }

            public void Eat()
            {
                Console.WriteLine("tweetybird eats {0}", eat);
                Console.ReadKey();

            }
            public void Clothes()
            {
                Console.WriteLine("tweetybird wears {0}", clothes);
                Console.ReadKey();
            }
            public void Age()
            {
                Console.WriteLine($"tweetybird's age is {age}");
                Console.ReadKey();
            }



        }
        public class bunny
        {
            private string speak;
            private string eat;
            private string clothes;
            private int age;

            public bunny(string bunnyspeak, string bunnyeat, string bunnyclothes, int bunnyage)
            {
                speak = bunnyspeak;
                eat = bunnyeat;
                clothes = bunnyclothes;
                age = bunnyage;
            }

            public void Speak()
            {
                Console.WriteLine("bugsbunny say {0}", speak);
                Console.ReadKey();
            }

            public void Eat()
            {
                Console.WriteLine("bugsbunny eats {0}", eat);
                Console.ReadKey();

            }
            public void Clothes()
            {
                Console.WriteLine("bugsbunny wears {0}", clothes);
                Console.ReadKey();
            }
            public void Age()
            {
                Console.WriteLine($"bugsbunny's age is {age}");
                Console.ReadKey();
            }





        }
        public class Duck
        {
            private string speak;
            private string eat;
            private string clothes;
            private int age;

            public Duck(string Duckspeak, string Duckeat, string Duckclothes, int Duckage)
            {
                speak = Duckspeak;
                eat = Duckeat;
                clothes = Duckclothes;
                age = Duckage;
            }

            public void Speak()
            {
                Console.WriteLine("daffyduck say {0}", speak);
                Console.ReadKey();
            }

            public void Eat()
            {
                Console.WriteLine("daffyduck eats {0}", eat);
                Console.ReadKey();

            }
            public void Clothes()
            {
                Console.WriteLine("daffyduck wears {0}", clothes);
                Console.ReadKey();
            }
            public void Age()
            {
                Console.WriteLine($"daffyduck's age is {age}");
                Console.ReadKey();
            }





        }

    }
}
