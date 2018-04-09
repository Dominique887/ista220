namespace MathsOperatorsch6

{

   

    public sealed partial class MainPage : Page

    {

        public MainPage()

        {

            this.InitializeComponent();

        }



        private void calculateClick(object sender, RoutedEventArgs e)

        {

            try

            {

                if ((bool)addition.IsChecked)

                {

                    addValues();

                }

                else if ((bool)subtraction.IsChecked)

                {

                    subtractValues();

                }

                else if ((bool)multiplication.IsChecked)

                {

                    multiplyValues();

                }

                else if ((bool)division.IsChecked)

                {

                    divideValues();

                }

                else if ((bool)remainder.IsChecked)

                {

                    remainderValues();

                }

                else

                {

                    throw new InvalidOperationException("No operator selected");

                }

            }

            catch (FormatException fEX)

            {

                result.Text = fEX.Message;

            }

            catch (InvalidOperationException ioEX)

            {

                result.Text = ioEX.Message;

            }

            catch (Exception ex)

            {

                expression.Text = "";

                result.Text = ex.Message;

            }

        }



        private void addValues()

        { try

            {

                int lhs = int.Parse(lhsOperand.Text);

                int rhs = int.Parse(rhsOperand.Text);

                int outcome = lhs + rhs;

                // TODO: Add rhs to lhs and store the result in outcome

                expression.Text = $"{lhsOperand.Text} + {rhsOperand.Text}";

                result.Text = outcome.ToString();

            }

            catch (FormatException fEX)

            {

                result.Text = fEX.Message;

            }

        } 



        private void subtractValues()

        {

            int lhs = int.Parse(lhsOperand.Text);

            int rhs = int.Parse(rhsOperand.Text);

            int outcome = lhs - rhs;

            // TODO: Subtract rhs from lhs and store the result in outcome

            expression.Text = $"{lhsOperand.Text} - {rhsOperand.Text}";

            result.Text = outcome.ToString();

        }



        private void multiplyValues()

        {

            int lhs = int.Parse(lhsOperand.Text);

            int rhs = int.Parse(rhsOperand.Text);

            int outcome = lhs * rhs;

            // TODO: Multiply lhs by rhs and store the result in outcome

            expression.Text = $"{lhsOperand.Text} * {rhsOperand.Text}";

            result.Text = outcome.ToString();

        }



        private void divideValues()

        {

            int lhs = int.Parse(lhsOperand.Text);

            int rhs = int.Parse(rhsOperand.Text);

            int outcome = lhs / rhs;

            // TODO: Divide lhs by rhs and store the result in outcome

            // expression.Text = $"{lhsOperand.Text} / {rhsOperand.Text}";

            expression.Text = lhsOperand.Text + " / " + rhsOperand.Text;

            result.Text = outcome.ToString();

        }



        private void remainderValues()

        {

            int lhs = int.Parse(lhsOperand.Text);

            int rhs = int.Parse(rhsOperand.Text);

            int outcome = lhs % rhs;

            // TODO: Work out the remainder after dividing lhs by rhs and store the result in outcome

            expression.Text = $"{lhsOperand.Text} % {rhsOperand.Text}";

            result.Text = outcome.ToString();

        }