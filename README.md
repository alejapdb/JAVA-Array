
# JAVA-Array
/*
 * Click nbfs://nbhost/SystemFileSystem/Templates/Licenses/license-default.txt to change this license
 */

package com.mycompany.matrices2_3;

import java.util.Scanner;

/**
 *
 * @author alejapdb
 */
public class Matrices2_3 {

    public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        System.out.println("Hello World!");
        
        int matriz1[][]= new int [4][4];
        int i;
        int j;
        
        for (i=0;i<matriz1.length; i++)
        {
            for (j=0;j<matriz1.length;j++)
            {
                System.out.println("Ingresa un dato ");
                matriz1[i][j]=sc.nextInt();
            }   
        }
        
         System.out.println("Selecciona una opcion ingresando el numero de la opcion:");
         System.out.println ("1.Suma de una fila" );
         System.out.println ("2. Suma de una columna" );
         System.out.println ("3. Sumar la diagonal principal " );
         System.out.println ( "4. Sumar la diagonal inversa " );
         System.out.println ("5. La media de todos los valores de la matriz");
         
         int opciones=sc.nextInt();
         
         int suma=0;
         int fila;
         int columna;
         int media=0;
        switch (opciones)
        {
        case 1:
            System.out.println ("Indica la fila que deseas sumar" );
            fila=sc.nextInt();
            for (i=0;i<matriz1.length;i++)
                {
                suma+=matriz1 [i][fila];
                }
            System.out.println ("la suma es" +suma);
            break;
            
            case 2:
             System.out.println ("Indica la columna que deseas sumar" );
            columna=sc.nextInt();
            for (j=0;j<matriz1.length;j++)
                {
                suma+=matriz1 [columna][j];
                }
            System.out.println ("la suma es" +suma);
            break;
            
            case 3:
            for (i=0;i<matriz1.length; i++)
        {
            for (j=0;j<matriz1.length;j++)
            {
                if(i==j)
                {
                suma+=matriz1 [i][j];
                }
            }
            System.out.println ("la suma es" +suma);
        }
            break;
            
            case 4:
            j=matriz1.length;
            for (i=0;i<matriz1.length; i++)
            {
                j-=1;
                suma+=matriz1 [i][j];    
            } 
             System.out.println ("la suma es" +suma);
             break;
            
            case 5:
            for (i=0;i<matriz1.length; i++)
            {
                for (j=0;j<matriz1.length;j++)
                {
                   suma+=matriz1 [i][j];  
                } 
            } 
            media=suma/(matriz1.length*matriz1.length);
            System.out.println ("la media es" +media);
            break;
        }
        
    }
}
