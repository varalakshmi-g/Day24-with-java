# Day24-with-java
Today I practiced how to print sub arrays with 

import java.util.Scanner;
public class Day24 {
    
    static void printSubArrays(int[] ar, int size)
    {
        for (int i = 0; i <= ar.length - size; i++)
        {
            for (int j = i; j < i + size; j++)
            {
                System.out.print(ar[j] + " ");
            }
            System.out.println();
        }
    }
    
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        int n = scan.nextInt();
        int[] ar = new int[n];
        for (int i = 0; i < ar.length; i++) {
            ar[i] = scan.nextInt();
        }
        int size = scan.nextInt();
        printSubArrays(ar, size);
    }
}
