# Day24-with-java
Today I practiced how to print sub arrays with size of 3. 
Here is the java program ...

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

Here is the output: 
Array size: 5
Array elements: 1 2 3 4 5
Size of the sub array: 3
Subarray :
(1 2 3)
(2 3 4)
(3 4 5)

