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


2] https://leetcode.com/problems/sort-colors/



Array (easy) 

class Solution {
    public void sortColors(int[] nums) {
        int zero=0;
        int first=0;
        int second=0;
        //count 0's 1's and 2's
        for(int i=0;i<nums.length;i++){
            if(nums[i]==0){
                zero++;
            }
            if(nums[i]==1){
                first++;
            }
            if(nums[i]==2){
                second++;
            }
        }
        for(int i=0;i<nums.length;i++){
            if(i<zero){
                nums[i]=0;
            }
            else if(i<(zero+first)){
                nums[i]=1;
            }
            else{
                nums[i]=2;
            }
        }
       
}
}

3] 
https://leetcode.com/problems/remove-duplicates-from-sorted-array/

(easy) (Array ,two pointers)

public class Solution {
    public int removeDuplicates(int[] nums) {
        int min=nums[0];
        int index=1;

        for (int i = 1; i < nums.length ; i++)
            if (nums[i]!=min){
                min=nums[i];
                nums[index]=min;
                index++;
            }
        return index;
    }
}
