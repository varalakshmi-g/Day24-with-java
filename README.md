# Day24-with-java
Today I practiced 
1. How to print sub arrays with size of 3. 
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

2. How to print the sum of sub arrays with the given size.

Here is the program to print sum of sub arrays

import java.util.Scanner;
public class Day24 {
    
    static void printSubArraysSum(int[] ar, int size)
    {
        for (int i = 0; i <= ar.length - size; i++)
        {
            int sum =0;
            for (int j = i; j < i + size; j++)
            {
                sum = sum + ar[j];
            }
            System.out.println(sum);
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
        printSubArraysSum(ar, size);
    }
}

Here is the output: 
Array size: 5
Array elements: 1 2 3 4 5
Size of the sub array: 3
sum :
6
9
12

3. How to print the count of sub arrays whose sum is equal to k.

Here is the program for the above ...

import java.util.Scanner;
public class Day24 {
    
    static void printSubArrays(int[] ar, int size, int k)
    {
        int count = 0;
        for (int i = 0; i <= ar.length - size; i++)
        {
            int sum =0;
            for (int j = i; j < i + size; j++)
            {
                sum = sum + ar[j];
            }
            if (sum == k)
            {
                count++;
            }
        }
        System.out.println(count);
    }
    
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        int n = scan.nextInt();
        int[] ar = new int[n];
        for (int i = 0; i < ar.length; i++) {
            ar[i] = scan.nextInt();
        }
        int size = scan.nextInt();
        int k = scan.nextInt();
        printSubArrays(ar, size, k);
    }
}


Here is the output: 
Array size: 5
Array elements: 1 2 3 4 5
Size of the sub array: 3
K : 9
count of sub arrays whose sum is equal to 9 : 1

4. Print the sub arrays whose sum is equal to k.

Here is he program...

import java.util.Scanner;
public class Day24 {
    
    static void printSubArrays(int[] ar, int size, int k)
    {
        for (int i = 0; i <= ar.length - size; i++)
        {
            int sum =0;
            for (int j = i; j < i + size; j++)
            {
                sum = sum + ar[j];
            }
            if (sum == k)
            {
                for (int j = i; j< i + size; j++)
                {
                    System.out.print(ar[j] + " ");
                }
                System.out.println();
            }
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
        int k = scan.nextInt();
        printSubArrays(ar, size, k);
    }
}

output: 
Array size: 5
Array elements: 1 2 3 4 5
Size of the sub array: 3
sum K : 9
sub arrays whose sum is equal to 9 : (2 3 4)






