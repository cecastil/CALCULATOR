# CALCULATOR
CALCULATOR PROGRAM
package com.company;
import java.util.Scanner;
public class Main {

    public static void main(String[] args) {
        int cal;
        Scanner sc = new Scanner(System.in);
        do {
            try {

                System.out.println("Calculadora sencilla");
                System.out.println("sumar (1), restar (2), dividir (3), multiplicar (4)");


                int operacion = sc.nextInt();
                if (operacion > 4) {
                    System.out.println("el valor ingresado no corresponde con una opcion");
                    System.out.println("sumar (1), restar (2), dividir (3), multiplicar (4)");
                    operacion = sc.nextInt();
                }
                if (operacion < 1) {
                    System.out.println("el valor ingresado no corresponde con una opcion");
                    System.out.println("sumar (1), restar (2), dividir (3), multiplicar (4)");
                    operacion = sc.nextInt();
                }

                System.out.println("Introduzca dos valores a para calcular");
                int a = sc.nextInt();
                int b = sc.nextInt();


                if (operacion == 1) {

                    double resultado = SUMA(a, b);
                    System.out.println("" + resultado);

                }
                if (operacion == 2) {

                    double resultado = RESTA(a, b);
                    System.out.println("" + resultado);

                }
                if (operacion == 3) {

                    double resultado = DIVISION(a, b);
                    System.out.println("" + resultado);

                }
                if (operacion == 4) {

                    double resultado = MULTIPLICACION(a, b);
                    System.out.println("" + resultado);

                }
                System.out.println("Quieres hacer otro calculo? Si(1) No(2)");
                cal = sc.nextInt();
            }catch (Exception e){System.out.println("valores no validos, deben ingresarse numeros enteros"); cal=1; sc.nextLine();}
        }while(cal==1);

    }
    public static int SUMA (int a, int b){
        return a+b;
    }
    public static int RESTA (int a, int b){
        return a-b;
    }
    public static int DIVISION (int a, int b){
        return a/b;
    }
    public static int MULTIPLICACION (int a,int b){
        return a*b;
    }
}
