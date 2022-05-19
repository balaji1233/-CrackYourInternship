# -CrackYourInternship
Arsh Goyal DSA sheet codes
Arrays:
1.	https://leetcode.com/problems/find-the-duplicate-number/

class Solution {

public  int findDuplicate(int[]arr)
  {
      int n=arr.length,res=-1;
      int[] count=new int[n];
      
      for(int i=0;i<n;i++)
         count[arr[i]-1]++;
      
      for(int i=0;i<n;i++)
        if(count[i]>=2)
        {
           res=i+1;
           break;
        }
             
       return res;
  }
  
    
}
