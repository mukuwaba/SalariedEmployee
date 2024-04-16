import org.hsqldb.jdbc.JDBCDataSourceFactory;

import java.sql.SQLOutput;

public class PayrollSystemTest {
    public static void main(String[] args) {
        SalariedEmployee salariedEmployee = new SalariedEmployee(
                "Ned",
                "Jones",
                "323-33-3212",
                10_000); //These are getting passed to the constructor and stored in the
                //new object
        System.out.printf("%n%s%n%s: $%, .2f%n%n", salariedEmployee, "earned", salariedEmployee.earnings());
    }//main
}//End: PayrollSystemTest
