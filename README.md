# CLAP2
Printing Pattern Using Loops
```
#include <stdio.h>
#include <string.h>
#include <math.h>
#include <stdlib.h>

int main() 
{

    int n;
    scanf("%d", &n);
  	// Complete the code to print the pattern.
     int len = n*2 - 1;
    for(int i=0;i<len;i++){
        for(int j=0;j<len;j++){
            int min = i < j ? i : j;
            min = min < len-i ? min : len-i-1;
            min = min < len-j-1 ? min : len-j-1;
            printf("%d ", n-min);
        }
        printf("\n");
    }
    return 0;
}
```
Project Euler #2: Even Fibonacci numbers
```
#include <math.h>
#include <stdio.h>
#include <string.h>
#include <stdlib.h>
#include <assert.h>
#include <limits.h>
#include <stdbool.h>

int main(){
    long int testcase;
 scanf("%ld",&testcase);
 while(testcase--)
 {
  long long int value,fact=0,temp=0,odd=1,even=2,count=0;
  scanf("%lld",&value);
  temp=value;
  while(temp--)
  {
   fact=odd+even;
   odd=even;
   even=fact;
   if(value>fact)
   {
   if(fact%2==0)
   count+=fact;
   }
   else
   break;
   
  }
  printf("%lld\n",count+2);
 }
    return 0;
}

```
Project Euler #4: Largest palindrome product
```
#include <math.h>
#include <stdio.h>
#include <string.h>
#include <stdlib.h>
#include <assert.h>
#include <limits.h>
#include <stdbool.h>

int palindrome(long int v)
{
   
 long int reverse,n,i,j;
    n=v;
    while (n != 0)
   {
      reverse = reverse * 10;
      reverse = reverse + n%10;
      n       = n/10;
   }
    if(reverse==v)
    {
     for(i=100;i<=999;i++)
         {
         for(j=100;j<=999;j++)
          {
           if(i*j==v)
               return 1;

         }
     }
        return 0;
    }
    else
        {
        return 0;
    }
}
int main() {

    int t;
    scanf("%d",&t);
    while(t--)
        {
        long int val;
        scanf("%ld",&val);
        int f=0;
        while(f==0)
            {
            f=palindrome(--val);
        }
        printf("%ld\n",val);
    }
    return 0;
}
```
Printing Tokens
```
#include <stdio.h>
#include <string.h>
#include <math.h>
#include <stdlib.h>

int main() {

     char *s;
    s = malloc(1024 * sizeof(char));
    scanf("%[^\n]", s);
    int len = strlen(s);

    for (int i = 0; i< len; i++)
    {    
        if (s[i]!=' ')
        {
            printf("%c", s[i]);
        }
        else{
            printf("\n");
        }
    }
    return 0;
}
```
Project Euler #1: Multiples of 3 and 5
```
#include <math.h>
#include <stdio.h>
#include <string.h>
#include <stdlib.h>
#include <assert.h>
#include <limits.h>
#include <stdbool.h>

int main(){
   unsigned long long n,sum=0,t;
    scanf("%llu",&t);
    while(t--)
        {
   
        scanf("%lld",&n);
        --n;
         unsigned long long n1,n2,n3;
         n1=n/3;
         n2=n/5;
         n3=n/15;
         sum=(3*n1*(n1+1))/2+(5*n2*(n2+1))/2-(15*n3*(n3+1))/2;
         printf("%lld\n",sum);
    }
    return 0;
}
```
