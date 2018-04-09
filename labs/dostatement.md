namespace DoStatement

{

    
    public sealed partial class MainPage : Page

    {

        public MainPage()

        {

            this.InitializeComponent();

        }



        private void showStepsClick(object sender, RoutedEventArgs e)

        {

            int amount = int.Parse(number.Text);

            steps.Text = "";

            string current = "";

        do

            {

                int nextDigit = amount % 8;

                amount /= 8;

                int digitCode = '0' + nextDigit;

                char digit = Convert.ToChar(digitCode);

                current = digit + current;

                steps.Text += current + "\n";

            }

        while (amount != 0);



        }