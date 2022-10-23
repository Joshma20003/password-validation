# password-validation
my first code
about password validation
----------------------------------------
#include <stdio.h>
#include<ctype.h>
int main()
{
	while(1)
	{
    char a[20];
    printf("give input password :: -> ");
    gets(a);
    int i=0,c1=0,c2=0,c3=0,c4=0;
    while(a[i]!=NULL){
    	if(islower(a[i]))
        {
        	c1+=1;
    	}
    	if(isupper(a[i]))
		{
    		c2+=1;
		}
		if(isdigit(a[i])){
			c3+=1;
		}
		if(!isalpha(a[i])&&!isdigit(a[i])){
			c4+=1;
		}
    	i++;
	} 
	printf("lower=%d\nupper=%d\ndigit=%d\nsymbol=%d\n",c1,c2,c3,c4);
	if(c1&&c2&&c3&&c4)
	{
	printf("Your Password is Vallied\n");
	break;
	}
	else
	printf("Your Password is NotVallied\n");
}
return 0;
}
