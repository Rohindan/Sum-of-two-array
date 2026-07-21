# Sum-of-two-array

import java.util.*;
public class Main{
    public static void main(String[] args){

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter a length for first array : ");
        int n1 = sc.nextInt();

        int[] arr1 = new int[n1];
        System.out.println("Enter "+ n1 +" numbers for your first array");
        for(int i = 0; i < arr1.length; i++){
            arr1[i] = sc.nextInt();
        }

        System.out.print("Enter a length for second array : ");
        int n2 = sc.nextInt();

        int[] arr2 = new int[n2];
        System.out.println("Enter "+ n2 +" numbers for your second array");
        for(int i = 0; i < arr2.length; i++){
            arr2[i] = sc.nextInt();
        }

        int[] sum = new int[n1 > n2 ? n1 : n2];

        int c = 0;
        int i = arr1.length-1;
        int j = arr2.length-1;
        int k = sum.length-1;

        while(k >= 0){
            int d = c;
            if(i >= 0){
                d += arr1[i];
            }
            if(j >= 0){
                d += arr2[j];
            }

            c = d/10;
            d = d%10;
            sum[k] = d;

            i--;
            j--;
            k--;
        }
        if(c >0 ){
            System.out.println(c);
        }
        for(int val: sum){
            System.out.println(val);
        }
    }
}
