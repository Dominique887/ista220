namespace Hello

{

   

    public sealed partial class MainPage : Page

    {

        public MainPage()

        {

            this.InitializeComponent();

        }



        private void okClick(object sender, RoutedEventArgs e)

        {

            MessageDialog msg = new MessageDialog("Hello " + userName1.Text);

            msg.ShowAsync();

        }



        private void textBlock_SelectionChanged(object sender, RoutedEventArgs e)

        {



        }