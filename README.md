# Euler-s-Method-
A prototype to Euler's Method that was discussed in Differential Equations
import java.util.Scanner;
/**
 *
 * @author Richard
 */
public class EulersMethod {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        Scanner i = new Scanner(System.in);
        double x =0;
        double h =0;
        
        System.out.println("What x value would you like to approximate");
        x = i.nextDouble();
        System.out.println("What height do you want to use for this approximaion?");
        h = i.nextDouble();
        
        double m =(int)(x);
        System.out.println("What is the 'y' value at x = "+m);
        double temp = i.nextDouble();
        double loop =Math.ceil((x-m)/h) ;
        System.out.println(loop);
        double solution = temp;
        for(int n =0;n<loop;n++){
           solution =  solution +Derivative(m,solution)*h;
           m=m+h;
           
           
}
        System.out.printf("The Given Information",solution);
     
        }

        
        // TODO code application logic here
    
    public static double Derivative(double x,double y){
                double answer =(x+y*y);
                   return answer;
    }
    
}
