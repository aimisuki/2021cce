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

## 第一題

設計一個程式，該程式可以連續讀入正整數(輸入0表示結束，至多不超過10個正整數)，之後將所輸入的正整數以相反序顯示在畫面上。 數字範圍：整數 1 – 1000

```c

#include <stdio.h>
int a[1000];
int main()
{
	int n;
	for(int i=0; i<=10; i++){
		scanf("%d", &a[i]);
		if(a[i]==0){
			n=i;
			break;
		}
	}
	for(int i=n-1; i>=0; i--){
		printf("%d ", a[i]);
	}
	printf("\n");
}

```

## 第二題

題目名稱：A的B次方函數
題目內容：請撰寫一個函數MYPOWER(A,B)，可以計算A^B結果。
數字範圍：整數 1 – 9。
程式限制：不得使用power()函數。不得變更已給定的主程式。

```c

#include <stdio.h>
int MYPOWER(int A, int B){
	int ans=1;
	for(int i=1; i<=B; i++){
		ans *= A;
	}
	return ans;
}
int main(void)
{
	int a,b;
	scanf("%d%d",&a,&b);
	printf("[%d]",MYPOWER(a,b));
	return 0;
}

```

## 第三題

輸入正整數n，計算1*2+2*3+3*4+…+(n-1)*n之和。 
數字範圍：整數1 – 1000

```c

#include <stdio.h>
int main()
{
	int a;
	int ans=0;
	scanf("%d", &a);
	for(int i=1; i<=a; i++){
		ans = ans+(i-1)*i;
	}
	printf("%d\n", ans);
}

```

## 第四題

撰寫一個程式要求使用者輸入矩形的長與寬，然後讀進這兩個整數。假如長與寬相同則印出訊息「It is a square」，否則印出訊息「It is not a square」。只能使用本章所學到的單一if敘述式。

```c

#include <stdio.h>
int main()
{
	int a, b;
	printf("Enter two numbers:  ");
	scanf("%d%d", &a, &b);
	if(a-b==0) printf("It is a square ");
	else printf("It is not a square ");
}

```

## 第五題

讀入一個0000 ~ 1111的2進位整數(固定4位數)，請顯示出對應的10進位數字。 
數字範圍：0000 – 1111

```c

#include <stdio.h>
int main()
{
	int a;
	int ans=0;
	scanf("%d", &a);
	if(a/1000==1) ans=ans+8;
	if(a%1000/100==1) ans=ans+4;
	if(a%100/10==1) ans=ans+2;
	if(a%10==1) ans=ans+1;
	printf("%d\n", ans);
}

```

## 第六題

輸入整數N, 再輸入N個同學的分數, 計算並且輸出均標(float 小數點後一位數), 均標是全部學生的平均分數, 再計算並且輸出前標(float 小數點後一位數), 本題的前標是大於或等於均標的同學的平均分數.

```c

#include <stdio.h>
int a[100];
int main()
{
	float n;
	float x=0;
	scanf("%f", &n);
	
	float ans=0;
	float sum=0;
	for(int i=0; i<n; i++){
		scanf("%d", &a[i]);
	}
	for(int i=0; i<n; i++){
		ans += a[i];
	}
	printf("均標:%.1f\n", ans/n);
	
	for(int i=0; i<n; i++){
		if(a[i]>=ans/n){
		sum += a[i];
		x++;
		}
	}
	printf("前標:%.1f\n", sum/x);
}


```
