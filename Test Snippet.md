public static void main(String[] args) {
    // Your database URL
    String databaseURL = "jdbc:ucanaccess://C:/Users/mukuwa.baffoe/Documents/Account.accdb";

    // Check if the user is logged in
    boolean isLoggedIn = false; // Initialize isLoggedIn as false
    // Prompt the user to log in or create an account
    System.out.println("Do you have an account?");
    System.out.println("Type:\n  login\n  create");
    Scanner loginput = new Scanner(System.in);
    String login = loginput.next();

    // Process login or account creation based on user input
    if (login.equals("login")) {
        // Code for user login
        // Your existing login code goes here
        // Set isLoggedIn to true if login is successful
    } else if (login.equals("create")) {
        // Code for creating a new account
        // Your existing account creation code goes here
        // Set isLoggedIn to true after creating the account
    }

    // If the user is logged in, display the contact manager GUI
    if (isLoggedIn) {
        SwingUtilities.invokeLater(() -> {
            Test gui = new Test();
            gui.setVisible(true);
        });
    }
}
//Ensure that you set the isLoggedIn variable to true if the login or account creation is successful.
// the contact manager GUI will only be displayed if the user is logged in. 
//Otherwise, they'll be prompted to log in or create an account.






