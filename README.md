# RateMyApp
Add a Dialog to your Android App asking your Customers to Rate Your App


Add the following Strings (Modify to fit your needs)

    <string name="dialog_message">Do you like My App? Please take the time to rate it.\n</string>
    <string name="dialog_message_yes">Yes</string>
    <string name="dialog_message_not_now">Not Now</string>
    <string name="dialog_message_never">Never</string>
    <string name="dialog_message_no_gp">You do not have Google Play installed</string>
    
    
    in your Main Class
      // Under    
      public class Main extends Activity  {
      
      // ADD 
      private RateMyApp rate;
    
      In onCreate add...
    
        //Initialize the RateMyApp component
        //set the title, days till the user is prompted and the no. of launches till the user is prompted
        rate = new RateMyApp(this, getString(R.string.app_name), 3, 3);
        //make all text white
        rate.setTextColor(Color.WHITE);
        //set message
        rate.setMessage(getString(R.string.dialog_message));
        //set text size
        rate.setTextSize(16);
        rate.start();
        
