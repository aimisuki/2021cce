# 2021cce
程設作業

##第一題

```c
#include <stdio.h>
int main()
{
	int n;
	scanf("%d", &n);
	printf("%d=50*%d+5*%d+1*%d\n", n, n/50, n%50/5, n%50%5);
}

```
#第二題

```c

#include <stdio.h>
int main()
{
	int n;
	scanf("%d", &n);
	int ans=0;
	for(int i=1; i<=n; i++){
		if(n%i==0){
			ans += 1;
		}
	}
	printf("%d\n", ans);
}

```
