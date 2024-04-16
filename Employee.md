//This is an inheritance AND abstract example
//w3schools c#
//abstract --> we do NOT instantiate! --> don't use keyword new/ make an object for the class
//         --> will be used as a parent for other classes, and those will be instantiated
public abstract class Employee {
    private final String firstName;
    private final String lastName;
    private final String socialSecurityNumber;

    //Constructor
    public Employee(String firstName,
                    String lastName,
                    String socialSecurityNumber){
        this.firstName = firstName;
        this.lastName = lastName;
        this.socialSecurityNumber = socialSecurityNumber;
    }//end Constructor

    public String getFirstName() {
        return firstName;
    }//end get first name

    public String getLastName() {
        return lastName;
    }//end get last name

    //g+TAB
    public String getSocialSecurityNumber() {
        return socialSecurityNumber;
    }//End get social

    @Override
    public String toString(){
        return String.format ("%s %s%nsocial security number: %s",
                getFirstName(),
                getLastName(),
                getSocialSecurityNumber());
    }

    public abstract double earnings();
}
    //abstract method that is going to return a double


