# 2021cce
程設作業

## 第一題

![1](https://github.com/aimisuki/2021cce/blob/gh-pages/1.png?raw=true)

```c
#include <stdio.h>
int main()
{
	int n;
	scanf("%d", &n);
	printf("%d=50*%d+5*%d+1*%d\n", n, n/50, n%50/5, n%50%5);
}

```

## 第二題

![2](https://github.com/aimisuki/2021cce/blob/gh-pages/2.png?raw=true)

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

## 第三題

![2](https://github.com/aimisuki/2021cce/blob/gh-pages/3.png?raw=true)

```c

#include <stdio.h>
int a[10];
int main()
{
	for(int i=0; i<10; i++){
		scanf("%d", &a[i]);
	}
	
	int ans=0;
	
	for(int i=0; i<10; i++){
		if(a[i]%3==0){
			ans += 1;
		}
	}
	printf("%d\n", ans);
}

```

## 第四題

![2](https://github.com/aimisuki/2021cce/blob/gh-pages/4.png?raw=true)

```c

#include <stdio.h>
int main()
{
	int n;
	scanf("%d", &n);
	if(n>=90) printf("A\n");
	else if(n<90&&n>=80) printf("B\n");
	else if(n<80&&n>=60) printf("C\n");
	else printf("F\n");

}

```
## 第五題

![2](https://github.com/aimisuki/2021cce/blob/gh-pages/5.png?raw=true)

```c
#include <stdio.h>
int main()
{
    int a, b, ans, temp;
    scanf("%d%d", &a, &b);

    if(b>a) temp=a;
    else temp=b;

    for(int i=1; i<=temp; i++){
        if(a%i==0&&b%i==0) ans=i;
    }

    printf("%d %d\n",a/ans, b/ans);

}


```
