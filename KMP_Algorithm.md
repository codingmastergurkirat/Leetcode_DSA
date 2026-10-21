Knuth Morris Pratt String Matching Algorithum

Suppose we have two strings 

string a = "abcabcabc"
string b = "abc"

if we try to check whether string b present in a or not using a naive approch then it's time complexity comes to be O(m*n), To Optimize it we will use KMP

KMP (Knuth Morris Pratt) Algorithum

Code for KMP Algorithm are as follows 

```
LPS[];
LPS[0] = 0;
Pattern[];
int i = 1;
int length = 0;
while(i < m ){
  if(Pattern[i]==Pattern[length]){
    length++;
    LPS[i] = length;
    i++;
  }else{
    if(length!=0){
      length--;
    }else{
     LPS[i] = 0;
    }
  }
}
```











