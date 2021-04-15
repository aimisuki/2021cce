# 2021cce
程設作業

## 第一題


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

## 第一題
1. 老師示範 int *p = &a[2]; *p=222; p = p + 2; *p = 666;
到底發生了什麼事? 請畫圖解釋

![1](https://github.com/aimisuki/2021cce/blob/gh-pages/week03-1.png)

## 第二題
2. 老師示範 int *p = &a[2]; *p=222; p = p + 2; *p = 666;
p--; *p=555;
到底發生了什麼事? 請畫圖解釋

![1](https://github.com/aimisuki/2021cce/blob/gh-pages/week03-2.png)

## 第三題
3. 老師把 int * p = &a[2] ; 的 p 心中的值(心裡放住址的小紙條) 印出來給你看 printf("%d\n", p);

![1](https://github.com/aimisuki/2021cce/blob/gh-pages/week03-3.png)

## 第四題
4. 4. 今天教最重要的是 malloc(), 它是什麼呢? 會幫你準備 memory (allocate memory)。請用老師傳給你的圖, 自己再畫一次, 增加印象。
    int * p;
    p = (int *) malloc( sizeof(int) * 10 );


![1](https://github.com/aimisuki/2021cce/blob/gh-pages/week03-4.png)

## 第一題

從鍵盤讀入1個4位數的整數(1000-9999)。如果該數字構成廻文(即由左而右，由右而左，順序相同)，則顯示YES。如果該數字未構成廻文，則顯示NO。

```c

#include <stdio.h>
int main()
{
	int n;
	scanf("%d", &n);
	
	int a=n;
	int ans=0;
	while(n!=0){
		ans = ans*10+n%10;
		n/=10;
	}
	
	if(ans==a) printf("YES\n");
	else printf("NO\n");
}

```

## 第二題

設計一個函數f(n)，該函數可以傳回整數n的數字反序排列所組成的整數。 
數字範圍：整數 1 – 9999 (不含10的倍數) 

```c

#include <stdio.h>
int ans=0;
int f(int n)
{
	while(n!=0){
		ans=ans*10+n%10;
		n/=10;
	}
	return ans;
}
int main()
{
	int a;
	scanf("%d", &a);
	printf("%d\n", f(a));
}

```

## 第三題

讀入一個正整數的數列(逐一輸入正整數，輸入0表示結束，數列至多包含10個整數)，之後再讀入一個正整數，程式可以找出該整數出現在數列中的次數。 
數字範圍：正整數 1 – 9 

```c

#include <stdio.h>
int a[10];
int main()
{
	int m, ans=0;
	
	for(int i=0; i<10; i++){
		scanf("%d", &a[i]);
		if(a[i]==0){
			break;
		}
	}
	
	scanf("%d", &m);
	
	for(int i=0; i<10; i++){
		if(a[i]==m) ans++;
	}
	printf("%d\n", ans);
}

```

## 第四題

寫一方法能傳入2個整數，如果第一個數字比第二個數字小，則回傳-1;如果兩個數字相等，則回傳0; 如果第一個數字比第二個數字大，則回傳1。印出比較後的結果。 

```c

#include <stdio.h>
int f(int a,int b){
	if(a>b) return 1;
	else if(a==b) return 0;
	else return -1;
}
int main(){
    int a, b;
    scanf("%d %d", &a, &b);
    printf("%d",f(a,b));
    return 0;
}


```

## 第五題

請撰寫一個程式計算並印出數個整數的加總。假設以999當成警示值。

```c

#include <stdio.h>
int a[10];
int main()
{
	int i, ans=0;
	for(i=0; i<100; i++){
		printf("Enter an integer ( 999 to end ): \n");
		scanf("%d", &a[i]);
		if(a[i]==999){
			break;
		}
	}
	for(int j=0; j<i; j++){
		ans += a[j];
	}
	printf("The total is: %d", ans); 
}
```

## 第六題

輸入兩個整數a b，輸出a除以b的餘數

```c

#include <stdio.h>
int main()
{
	int n, m;
	scanf("%d%d", &n, &m);
	printf("%d", n%m);
	
}

```

## 第七題

輸入一個整數成嫧，如果所輸入的整數大於或等於90，則輸出A; 如果輸入的整數小於90但大於等於80，則輸出B;如果小於80但大於或等於70，則輸出C;如果小於70但大於或等於60，則輸出D;如為其他整數則輸出F。 

```c

#include <stdio.h>
int main()
{
	int n;
	scanf("%d", &n);
	
	if(n>=90) printf("A");
	else if(n<90&&n>=80) printf("B");
	else if(n<80&&n>=70) printf("C");
	else if(n<70&&n>=60) printf("D");
	else  printf("F");
}
```

## 第八題

輸入里程公尺數，輸出應付的車資。計程車資計算方式為: 起跳100元(1500公尺)，續跳5元(每250公尺)註:不足250公尺也要5元。 

```c

#include <stdio.h>
int main()
{
	int n;
	scanf("%d", &n);
	if(n>1500&&n/250!=0) n=(n-1500)/250+1;
	printf("%d", 100+n*5);
}

```

## 第九題

假設有50元、10元、5元和1元等4種硬幣，請輸入一個金額，並顯示等同於該金額所需的最少硬幣組合。

```c

#include <stdio.h>
int main()
{
	#include <stdio.h>
int main()
{
	int n;
	scanf("%d", &n);
	printf("%d=50*%d+10*%d+5*%d+1*%d", n, n/50, n%50/10, n%10/5, n%5);
}

```
