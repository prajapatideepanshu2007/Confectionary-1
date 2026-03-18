# Confectionary-1
My first c program
<br>
#include<stdio.h>
#include<string.h>
void menu();
void order();
void presentation();
void main()
{
int i=1,sum=0,k1=0,k2=0,k3=0,k4=0,k5=0,k6,l1=1,t=1;
char a[12], b[6]="Sugar",c[12]="Tea leaves",d[10]="Biscuit",e[10]="Namkeen",f[6]="Chips",g[5]="Bill";
  
//Presentation of shop  //seeing menu to consumer
presentation();
menu();

//taking order
printf("\n\nEnter your %d choice : ",t);
gets(a);



//Calculating Price
for(int k=0;k<100;k++)
{
  int l = strlen(a);
if(strncmp(a,b,l)==0||strncmp(a,b,l)==128)
{
sum=sum+50;
k1++;
}
else if(strncmp(a,c,l)==0||strncmp(a,c,l)==128)
{
sum=sum+200;

k2++;
}
else if(strncmp(a,d,l)==0||strncmp(a,d,l)==128)
{
sum=sum+10;
k3++;
}
else if(strncmp(a,e,l)==0||strncmp(a,e,l)==128)
{
sum=sum+20;
k4++;
}
else if(strncmp(a,f,l)==0||strncmp(a,f,l)==128)
{
sum=sum+5;
k5++;
}

//Billing
if(strncmp(a,g,l)==0||strncmp(a,g,l)==128)
{
printf("\n\n***Deepanshu Confectionary Bill***\n");
//printf("\nS.No. No.of item  Name of item Amount(Rs)");
if(k1>0)
{
  printf("\n%d. %d Sugar = %dRs",l1,k1,k1*50);
  l1++;
}
if(k2>0)
{
  printf("\n%d. %d Tea leaves = %dRs",l1,k2,k2*200);
  l1++;
}
if(k3>0)
{
  printf("\n%d. %d Biscuit = %dRs",l1,k3,k3*10);
  l1++;
}
 if(k4>0)
{
  printf("\n%d. %d Namkeen = %dRs",l1,k4,k4*20);
  l1++;
}
 if(k5>0)
{
  printf("\n%d. %d Chips = %dRs",l1,k5,k5*5);
  l1++;
}
printf("\n\n*************************************");
printf("\n\nYour Total Amount of %d order is : %d Rs",k1+k2+k3+k4+k5,sum);
printf("\nThank You for order! Please Visit Again.\nHave a Nice Day😇😁👍🏻.");
break;
}


//order is available or not
if (strcmp(a,b)!=0&&strcmp(a,c)!=0&&strcmp(a,d)!=0&&strcmp(a,e)!=0&&strcmp(a,f)!=0&&strcmp(a,g)!=0&&strcmp(a,b)!=128&&strcmp(a,c)!=128&&strcmp(a,d)!=128&&strcmp(a,e)!=128&&strcmp(a,f)!=128&&strcmp(a,g)!=128) 
{
  printf("!!Invalid Choice/Order not available!!");
  i--;
}


//taking order again
order();
i++;
t++;
printf("\nEnter Your %d choice : ",t);
scanf("%s",a);
}
}



void order()
{
printf("\n\n1. Sugar - 50₹/kg\n2. Tea leaves - 200₹/kg\n3. Biscuit - 10₹/piece");
printf("\n4. Namkeen - 20₹/100gm\n5. Chips - 5₹/packet\n6.For Billing - Bill\n\n");
}

void presentation()
{  //Presentation of shop  
printf("\n  *************************************\n  *                                   *\n  *");
  printf("      DEEPANSHU CONFECTIONARY      *\n  *                                   *\n  *************************************\n");
 printf("\nWelcome to Deepanshu's Confectionary!"); 
  //seeing menu to consumer
printf("\n\nHere is our menu ---\n");
printf("Enter the product name whatever you want");
}

void menu()
{
  printf("\n\n1. Sugar - 50₹/kg\n2. Tea leaves - 200₹/kg\n3. Biscuit - 10₹/piece");
printf("\n4. Namkeen - 20₹/100gm\n5. Chips - 5₹/packet\n\n");
}
