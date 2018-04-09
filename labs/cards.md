namespace Cards

{

    

    public sealed partial class MainPage : Page

    {

        public const int NumHands = 4;

        private Pack pack = null;

        private Hand[] hands = new Hand[NumHands];



        public MainPage()

        {

            this.InitializeComponent();

        }



        private void dealClick(object sender, RoutedEventArgs e)

        {

            try

            {

                pack = new Pack();

                for (int handNum = 0; handNum < NumHands; handNum++)

                {

                    for (int numCards = 0; numCards< Hand.HandSize; numCards++)

                    {

                        PlayingCard cardDealt = pack.DealCardFromPack();

                        hands[handNum].AddCardToHand(cardDealt);

                    }

                    north.Text = hands[0].ToString();

                    south.Text = hands[1].ToString();

                    east.Text = hands[2].ToString();

                    west.Text = hands[3].ToString();

                }



            }

            catch (Exception ex)

            {

                MessageDialog msg = new MessageDialog(ex.Message, "Error");

                msg.ShowAsync();

            }