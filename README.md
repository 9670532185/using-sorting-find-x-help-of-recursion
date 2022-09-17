# using-sorting-find-x-help-of-recursion
public class BinarySearchRec {
    public static int Print(int arr[],int s,int e,int x)
    {
       // int x=4;
       // int le=arr.length;
        //int s=0;
        //int e=le-1;
   
        if(s>e)
        {
            //if(arr[mid]==x)
            return -1;
        }
        int mid=(s+e)/2;
        if(arr[mid]==x)
        {
            return mid;
        }
          else if(arr[mid]<x)
        {
         return Print(arr,mid+1,e,x);
        }
        else{
            return Print(arr,s,mid-1,x);
        }
    }
    public static void main(String[] args)
    {
int[] arr={1,2,3,4};
 int pe=Print(arr,0,arr.length-1,4);
 System.out.println(pe);
    }
    
}
