namespace Selection

{

    

    public sealed partial class MainPage : Page

    {

        public MainPage()

        {

            this.InitializeComponent();

        }



        private void compareClick(object sender, RoutedEventArgs e)

        {

            int diff = dateCompare(firstDate.Date.LocalDateTime, secondDate.Date.LocalDateTime);

            info.Text = "";

            show("firstDate == secondDate", diff == 0);

            show("firstDate != secondDate", diff != 0);

            show("firstDate <  secondDate", diff < 0);

            show("firstDate <= secondDate", diff <= 0);

            show("firstDate >  secondDate", diff > 0);

            show("firstDate >= secondDate", diff >= 0);

        }



        private void show(string exp, bool result)

        {

            info.Text += exp;

            info.Text += " : " + result.ToString();

            info.Text += "\n";

        }



        private int dateCompare(DateTime leftHandSide, DateTime rightHandSide)

        {

            int result = 0;

            

            if (leftHandSide.Year < rightHandSide.Year)

            {

                result = -1;

            }

            else if (leftHandSide.Year > rightHandSide.Year)

            {

                result = 1;

            }

            else if (leftHandSide.Month < rightHandSide.Month)

            {

                result = -1;

            }

            else if (leftHandSide.Month > rightHandSide.Month)

            {

                result = 1;

            }

            else if (leftHandSide.Day < rightHandSide.Day)

            {

                result = -1;

            }

            else if (leftHandSide.Day > rightHandSide.Day)

            {

                result = 1;

            }

            else

            {

                result = 0;

            }



            return result;

        }

    }