# Given-an-array-which-consists-of-only-0-1-and-2.-Sort-the-array-without-using-any-sorting-algo
import java.util.*;
public class Main{
    static void sort123(int arr[],int arr_size)
    {
        int l=0;
        int h=arr_size-1;
        int m=0;
        int temp=0 ;
        
        while(m<=h)
        {
            switch(arr[m])
            {
                case 0:
                    {
                        temp=arr[l];
                        arr[l]=arr[m];
                        arr[m]=temp;
                        l++;
                        m++;
                        break;
                    }
                    
                case 1:
                        m++;
                        break;
                
                case 2:
                    {
                        temp=arr[m];
                        arr[m]=arr[l];
                        arr[h]=temp;
                        h--;
                        break;
                    }
                
            }
        }
    }
    
    static void printArray(int arr[],int arr_size)
    {
        for(int i=0;i<arr_size;i++)
        {
            System.out.println(arr[i]+" ");
            
            System.out.println(" ");
        }
    }
    public static void main(String args[])
    {
        int arr[]={1,2,0,0,2,2,1,2,1,0,2};
        int arr_size=arr.length;
        sort123(arr,arr_size);
        printArray(arr,arr_size);
    }
}
