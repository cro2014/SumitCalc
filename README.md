# SumitCalc


import java.util.Scanner;

public class SimpileCalculator {
    private static Scanner scan=new Scanner(System.in);

    public static void main(String[] args) {
      SimpileCalculator cal=new SimpileCalculator();
      System.out.println("enter num1");
      int num1=scan.nextInt();
      System.out.println("enter the opertion");
      String operation=scan.next();
      System.out.println("enter num2");
      int num2=scan.nextInt();
      while(true){
          String res=cal.calculate(num1,operation,num2);
            if(res.equals("invalid")){
                System.out.println("invalid opertion");
                break;
            }else {
                num1 = Integer.parseInt(res);
                System.out.println(num1);
                System.out.println("enter the opertion");
                operation = scan.next();
                System.out.println("enter num2");
                num2 = scan.nextInt();
            }
      }

    }

    public  String calculate(int num1,String operataion,int num2){
        switch (operataion){
            case "+":
                return ""+add(num1,num2);
            case "-":
                return ""+sub(num1,num2);


            case "*":
                return ""+mul(num1,num2);


            case "/":
                return ""+div(num1,num2);


            default:

                return  "invalid";


        }
    }

    public int add(int num1 ,int num2){
        return num1+num2;
    }

    public int sub(int num1, int num2){
        return num1-num2;
    }

    public int div(int num1,int num2){
        return num1/num2;
    }

    public int mul(int num1, int num2){
        return num1*num2;
    }
}
