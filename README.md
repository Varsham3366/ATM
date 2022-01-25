#include <stdio.h>
struct employee
{
    char e_name[25];
    int e_idno,bpay,gpay,npay;
    float hra,da,pf;
};
void main()
{
    
    int n_emp;
    printf("Enter the number of employee to be added");
    scanf("%d",&n_emp);
    
   struct employee emp[n_emp];
    for(int i=0;i<n_emp;i++)
    {
    printf("\n Enter EMPLOYEE NAME       : ");
    scanf("%s",emp[i].e_name);
    printf("\n Enter EMPLOYEE ID NUMBER  : ");
    scanf("%d",&emp[i].e_idno);
    printf("\n  Enter EMPLOYEE BASIC PAY : ");
    scanf("%d",&emp[i].bpay);
    
    {
        
        if(emp[i].bpay<25000)
        {
            emp[i].hra=emp[i].bpay*10/100;
            emp[i].da=emp[i].bpay*20/100;
            emp[i].pf=1000;
        }
        else if(emp[i].bpay>=25000 && emp[i].bpay<40000)
        {
            emp[i].hra=emp[i].bpay*20/100;
            emp[i].da=emp[i].bpay*30/100;
            emp[i].pf=1500;
        }
        else if(emp[i].bpay>=40000)
        {
            emp[i].hra=emp[i].bpay*25/100;
            emp[i].da=emp[i].bpay*35/100;
            emp[i].pf=2000;
        }
     emp[i].gpay=emp[i].bpay+emp[i].hra+emp[i].da;
     emp[i].npay=emp[i].gpay-emp[i].pf;
     
     {
         
         
         printf("\n\n *** PAY BILL *** \n\n ");
         printf("\n EMPLOYEE NAME       :%s",emp[i].e_name);
         printf("\n EMPLOYEE ID NUMBER  : %d",emp[i].e_idno);
         printf("\n EMPLOYEE BASIC PAY  :%d",emp[i].bpay);
         printf("\n GROSS PAY           :%d",emp[i].gpay);
         printf("\n NET PAY             :%d",emp[i].npay);
         printf("\n\n address of employee in memory :%p",&emp[i].e_name);
     }
}
    } 
    char s[20]="THANK YOU";
    printf("\n\n %s",s);
    fflush(stdin);
    }
