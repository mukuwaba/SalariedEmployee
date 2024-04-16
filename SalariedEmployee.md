//This class will inherit
public class SalariedEmployee extends Employee {
    //SalariedEmployee will 'inherit from' Employee
    //entends--> inherits from
    private double weeklySalary;

    //Constructor
    public SalariedEmployee(String firstName, String lastName, String socialSecurityNumber, double weekySalary){
        super(firstName, lastName, socialSecurityNumber); //passes these values up to the parent constructor

        //validation step...
        if(weekySalary < 0.0){
            throw new IllegalArgumentException("Weekly salary must be >= 0.0");
        }//End; if

        this.weeklySalary = weekySalary;

    }//SalariedEmployee Constructor End

    public void setWeeklySalary(double weeklySalary) {
        if (weeklySalary < 0.0){
            throw new IllegalArgumentException("Weekly salary must be >= 0.0");
        }
        this.weeklySalary = weeklySalary;
    }

    public double getWeeklySalary() {
        return weeklySalary;
    }
    @Override //want to override parents with our own earnings method
    public double earnings() {
        return getWeeklySalary();}

    @Override
    public String toString(){
        return String.format("salaried employee: %s%n%s: $%, .2f",
                super.toString(), "weekly salary", getWeeklySalary());
        }//end: return
    }//SalariedEmployee

