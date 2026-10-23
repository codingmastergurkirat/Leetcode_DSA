> AND operation of every two numbers is always equal to or less then the smaller number

we have to just find the numbers that is not equal to its index and then perform AND opertaion on all of them to find k

Initialize k with -1 because in -1 all bits are set

then start and operation on numbers with k which are not on the correct position or we can say not equal to the index

the code looks like below
```
class Solution {
public:
    int sortPermutation(vector<int>& nums) {
        int n = nums.size();
        int k = -1;

        for(int i = 0 ; i < n ; i++){
            if(nums[i]!=i){
                k = k & nums[i];
            }
        }
        return (k==-1?0:k);
    }
};
```

