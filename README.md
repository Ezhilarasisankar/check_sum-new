# check_sum-new
just another repository
#include<stdio.h>
#include<string.h>
#include<math.h>
#include<stdlib.h>
int convertBinaryToDecimal(int p[],int n)
{
    int decimalNumber = 0, i = 0, remainder,j;
    int base;base=1;int k;
    int p1[n],h;h=0;
    for(k=n-1;k>=0;k--)
    {
    	p1[h]=p[k];
    	h++;
	}
	for(j=0;j<n;j++)
    {
	
	
	
	if(p1[j]==0||p1[j]==1)
    {
        int last_digit = p1[j] % 10;
        p1[j] = p1[j]/10;
         decimalNumber += last_digit*pow(2,i);
        i++;
        //decimalNumber += last_digit*base;
         
        //base = base*2;
    }

    /*while (p[j]!=0)
    {
        remainder = p[j]%10;
        p[j] /= 10;
        decimalNumber += remainder*pow(2,i);
        ++i;
    }*/
	}
    return decimalNumber;
}


main()
{
char data[50],d[50];
int par[100],da[100],c1[100],st[100],temp[100],da1[100];
int i,n2,q,h,p,n1,j,k,l,m,in,n,len,app,app1,h1;
int bin,ca,appf,appfs,len1,s,b,u,v,x,ori_da[100],ori_data[100];
char *d1;
j=0;k=0;in=0;l=0;h1=0;
int sum;sum=0;
FILE *fp;
fp=fopen("checksend.txt","w");
printf("\nEnter data:");
scanf("%s",data);
len=strlen(data);
app1=len%8;
/*if(app1!=0)
{
app=8-app1;

for(i=0;i<app;i++)
{par[i]=0;
in++;
}
}*/
k=0;
for(i=0;i<len;i++)
{
par[i]=data[k]-'0';
k++;
}
n=k;
printf("\n");
for(h=0;h<n;h++)
{
	//printf("%d",par[h]);
// bin=par[h];
}
/*q=(len+app)/8;
for(i=0;i<8;i++)
{j=i;
count=0;
for(m=0;m<q;m++)
{
j+=8;*/
/*for(i=len;i>=0;i--)
{
	if(i%8==0)
	{
				if(par[i]==1 && flag==0)
		{
			flag = 1;
			continue;
		}
		if(par[i]==0 && flag==0)
		{
			continue;
		}
		if(par[i]==1)
			c[i]=0;
		else
			c[i]=1;
	}
else{
	continue;
}*/

/*for(i=0;i<len;i++){
    p=10;

    while(par[i]>=p)
        p*=10;

    bin*=p;  
    bin+=par[i];
}*/

/*long i1;
long j1;
long n1;
long k1;

i1 = len;
j1 = 0;
n1 = 0;
k1 = 1;
while( 1 )
{
    if( j1 == 0 )
    {
        i1--;
        if( i1 < 0 )
        {
            break;
        }
        j1 = par[ i1 ];
    }

    n1 += ( j1 % 10 ) * k1;
    j1 /= 10;
    k1 *= 10;
}

printf("%ld\n", n1);*/ // <== final result printed
app=len%8;
if(app!=0)
app1=8-app;	
for(ca=len;ca<len+app1;ca++)
{
	par[ca]=0;
	}
/*for(m=0;m<len+app1;m++)
{
	if(par[m]==0)
	 par[m]=1;
	else
	 par[m]=0;
}

printf("\n");
	for(m=0;m<len+app1;m++)
	{
		printf("%d",par[m]);
	}*/
	
	
		
	/*for(ca=0;ca<len+app1;ca++)
	{
		printf("%d",par[ca]);
	}*/
	
	//for(ca=0;ca<len+app1;ca=ca+8)
	//{
	
	
	
	
m=0;	
	q=(len+app1)/8;
//for(m=0;m<q;m++)
//{//k=i;
//count=0;
printf("\n");
k=0;
//for(i=0;i<8;i++)
for(i=0;i<len+app1;i++)
{
	//k=i;
	printf("%d",par[i]);
	temp[k]=par[i];
	k++;
	if((i+1)%8==0)
	{
	
		bin=convertBinaryToDecimal(temp,8);
//if(arr1[k]==1)
//{count+=1;}
		sum+=bin;
		k=0;
//m++;
//k+=8;
	}
}
printf("%d",sum);
//itoa(sum,d,2);
//res[i]=count%2;}

//fp=fop
/*k=0;
for(m=0;m<8;m++)
{
	da[k]=d[m]-'0';
	k++;
}*/
 s = 0;
    while (sum > 0) {
 
        // storing remainder in binary array
        d[s] = sum% 2;
        sum = sum / 2;
        s++;
    }n1=s;
 printf("\n");
    // printing binary array in reverse order
    for ( u =s-1; u >=0; u--)
        printf("%d",d[u]);
/*k=7;
for(m=0;m<8;m++)
	{
		if(k>=0)
		{
			d[m]=d[k];
			k--;
		}
	}*/
	for(k=n1-1;k>=0;k--)
    {
    	da1[h1]=d[k];
    	h1++;
	}

	i=0;
for(m=7;m>=0;m--)
{
	if(d[m]==0)
	 da[i]=1;
	else
	 da[i]=0;
i++;
}

printf("\n");
	for(m=0;m<8;m++)
	{
		printf("%d",da[m]);
	}
	
	
	bin=convertBinaryToDecimal(da,8);
//}
//sum+=bin;
	printf("\n%d",bin+1);
	v=bin+1;
 x = 0;
    while (v > 0) {
 
        // storing remainder in binary array
        ori_da[x] = v % 2;
        v = v / 2;
        x++;
    }
n2=x;
 printf("\n");
    // printing binary array in reverse order
    for ( b = x - 1; b >= 0; b--)
        printf("%d",ori_da[b]);

printf("\n");
for(i=0;i<len+app1;i++)
{
	fprintf(fp,"%d",par[i]);
}
for(b=n2;b>=0;b--)
{
	fprintf(fp,"%d",ori_da[b]);
}


/*appf=n2%8;
appfs=8-appf;
for(i=0;i<appfs;i++)
{   
    //ori_data[i]=ori_data[i+1]; 
 	 ori_data[i]=ori_da[i+1];
	 ori_data[i]=0;
 	//ori_data[i]=ori_data[i+1];
}	
for(i=appfs;i<n2;i++)
{
	ori_data[i]=ori_da[in];
	in++;
	}	
	
	for(i=0;i<n2;i++)
	{
		printf("%d",ori_data[i]);
	}*/
	
	
	
	
	//itoa(bin+1,d1,2);
	/*printf("\n%s",d1);
	len1=strlen(d1);
	m=0;
	for(m=0;m<len1;m++)
	{
		ori_da[l]=d1[m]-'0';
		l++;
		}	
		for(i=0;i<l;i++)
		{
			printf("%d",ori_da[i]);
		}*/
	//printf("%ll",bin);
	/*for(i=0;i<8;i++)
	{
		printf("%d",c[i]);
	}*/


/*for(i=0;data[i]!='\0';i++)
{
par[j][k]=data[i];
if(i%8==0)
{
//c[j][k]=(int)(par[j][k]|par[j+1][k]);
if(par[j][k]=='0')

j++;
k++;
if(c[j][k]=='0')
{c[j][k]='1';}
else
{c[j][k]='0';}
c1[j][k]=c[j][k]|00000001;
st[j][k]=c1[j][k];
}
}
//fputs(st,fp);
for(l=0;l<j;l++)
{
	for(m=0;m<k;m++)
	{
		printf("\t%c",c[j][k]);
		printf("\t%c",c1[j][k]);
		printf("\t%c",st[j][k]);
		fprintf(fp,"%c",st[j][k]);
	}
}*/


fclose(fp);
}
