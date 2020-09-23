<div align="center">

## Gauss Seidel\(Solutions of Equations\)


</div>

### Description

There method can be used to solve a set of linear equations that are based on iteration. This is an optimized jacobi iteration.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Akash Khaitan](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/akash-khaitan.md)
**Level**          |Advanced
**User Rating**    |5.0 (10 globes from 2 users)
**Compatibility**  |C
**Category**       |[Math](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/math__3-12.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/akash-khaitan-gauss-seidel-solutions-of-equations__3-13629/archive/master.zip)





### Source Code

```
#include<stdio.h>
int main(void)
{
	float a[10][10],b[10],x[10],y[10];
	int n=0,m=0,i=0,j=0;
	printf("Enter size of 2d array(Square matrix) : ");
	scanf("%d",&n);
	for(i=0;i<n;i++)
	{
		for(j=0;j<n;j++)
		{
			printf("Enter values no. %d %d :",i,j);
			scanf("%f",&a[i][j]);
		}
	}
	printf("\nEnter Values to the right side of equation\n");
	for(i=0;i<n;i++)
	{
			printf("Enter values no. %d :",i,j);
			scanf("%f",&b[i]);
	}
	printf("Enter initial values of x\n");
	for(i=0;i<n;i++)
	{
		printf("Enter values no. %d :",i);
		scanf("%f",&x[i]);
	}
	printf("\nEnter the no. of iteration : " );
	scanf("%d",&m);
	while(m>0)
	{
		for(i=0;i<n;i++)
		{
			y[i]=(b[i]/a[i][i]);
			for(j=0;j<n;j++)
			{
				if(j==i)
					continue;
				y[i]=y[i]-((a[i][j]/a[i][i])*x[j]);
				x[i]=y[i];
			}
			printf("x%d = %f	",i+1,y[i]);
		}
		printf("\n\n");
		m--;
	}
	return 0;
}
```

