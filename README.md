Working ATM in Java by BeriiiOsu
Heres: The "Main" code
Other files are in the zip!!!


package automatedtellermachine;
import java.util.*;
import java.io.*;
public class AutomatedTellerMachine {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Register r = new Register();
        accountNumberGenerator ag = new accountNumberGenerator();
        Login lg = new Login();
        
        
        
        
        
        System.out.println("        ::::::::::::::::::::::::::::::::::::::");
        System.out.println("        ::            xxx ATM xxx           ::");
        System.out.println("        ::                                  ::");
        System.out.println("        :: 1. Enter                         ::");
        System.out.println("        :: 2. Exit                          ::");
        System.out.println("        ::                                  ::");
        System.out.println("        ::                                  ::");
        System.out.println("        ::::::::::::::::::::::::::::::::::::::");
        System.out.print  ("        : ");
        try{
        int input = sc.nextInt();
        if(input <= 0){
            System.out.println("Invalid Input!!");
            System.exit(0);
        }
        //welcome screen 
        if(input == 1){
            
        System.out.println("        ::::::::::::::::::::::::::::::::::::::");
        System.out.println("        ::            xxx ATM xxx           ::");
        System.out.println("        ::                                  ::");
        System.out.println("        :: 1. Register an Account           ::");
        System.out.println("        :: 2. Enter Account Number          ::");
        System.out.println("        :: 3. Exit                          ::");
        System.out.println("        ::                                  ::");
        System.out.println("        ::::::::::::::::::::::::::::::::::::::");
        System.out.print  ("        : ");
        int input2 = sc.nextInt(4);
        try{
            if(input2 <= 0){
                System.out.println("Invalid Input!!");
            }
            else if(input2 == 1){
                System.out.print(" Enter Firstname               : ");
                String fname = sc.next();
                System.out.print(" Enter Middlename              : ");
                String mname = sc.next();
                System.out.print(" Enter Lastname                : ");
                String lname = sc.next();
                System.out.print(" Enter Age                     : ");
                int age = sc.nextInt();
                System.out.print(" Enter your PIN                : ");
                int pin = sc.nextInt();
                
                System.out.println();
                ag.an();
                String accnum = accountNumberGenerator.generateAccountNumber;
                
                String fullname = fname + " " + mname + " " + lname;
                System.out.println(" Check your details:");
                System.out.println(" Fullname                    : " + fullname);
                System.out.println(" Age                         : " + age);
                System.out.println(" PIN                         : " + pin);
                System.out.println(" Account Number              : " + accnum);
                
                r.registerAccount(fullname, age, pin);
                
            }
            else if(input2 == 2){
                lg.loginAndOperate();
            }
            else if(input2 == 3){
                System.out.println("Exiting...");
                System.exit(0);
            }
        }catch(Exception e){
                    System.out.println("Invalid Input!!");
                    }
        
        
        
        }
        else if (input == 2){
            System.out.println("Exiting...");
            System.exit(0);
        }
        }catch(Exception e){
            System.out.println("Invalid Input!!");
        }
        
    }
    
}

