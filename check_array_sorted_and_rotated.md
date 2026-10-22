To check that array is sorted and rotated we have to just check one condition and that condition are as follows:

```
if ( nums[i] > nums[i+1]%n ) {
  count++;
}
```

if count > 1 then it is not sorted other wise it is sorted:
because no matter it is rotated there must be one place where the above condition satisfy in the sorted array
