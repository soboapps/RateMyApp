# RateMyApp
Add a Dialog to your Android App asking your Customers to Rate Your App

1. Copy the RAteMyApp.class file to your Project (Don't foreget to Modify the Package Name at the Top)

2. Add the following Strings (Modify to fit your needs)

    <string name="dialog_message">Do you like My App? Please take the time to rate it.\n</string>
    <string name="dialog_message_yes">Yes</string>
    <string name="dialog_message_not_now">Not Now</string>
    <string name="dialog_message_never">Never</string>
    <string name="dialog_message_no_gp">You do not have Google Play installed</string>
    
3. in your Main Class
      // Under your    
      public class Main...
      
      // Add... 
      private RateMyApp rate;

    
4. In onCreate Add...
    
        //Initialize the RateMyApp component
        //rate = sets the title (getString(R.string.app_name), 3 (days until the user is prompted)
        //, 3 (number of launches until the user is prompted)
        rate = new RateMyApp(this, getString(R.string.app_name), 3, 3);
        //make all text white
        rate.setTextColor(Color.WHITE);
        //set message
        rate.setMessage(getString(R.string.dialog_message));
        //set text size
        rate.setTextSize(16);
        rate.start();
        
