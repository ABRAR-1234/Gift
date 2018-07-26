# Unique program
package com.abr;

public class Main {

    public static void main(String[] args)
    {
     int var = position(7600);
        System.out.println("The distance from house to gift position" + var);
    }
    private static boolean isPrime(int n)
    {
        if( n == 1)
        {
            return false;
        }
        for(int i=2 ; i<=n/2 ; i++)
        {
            return true;
        }
        return true;
    }
    private static int position(int s)
    {
        int pos = 1;
        int count = 0;
        while(s > 0) {
            int number = s % 10;
            s /= 10;
            count++;
            if (isPrime(s)) {
                pos = count + 1;
            }
        }
        return pos;
    }
}



