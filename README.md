# sequential_search
A function that searches sequentially for the numbers you want to search in arrays.


#include <stdio.h>
#include <stdlib.h>

int sequential_search(int arr[],int search,int size)
{
int i = 0;
	
while(i < size)
{
	if(arr[i] == search)
		return (i);
	else
		i++;
	}
return -1;
}


int main()
{
int arr[] = {12,15,16,17,18,19,29,57};
int size = sizeof(arr) / sizeof(arr[0]);
int search;
	
printf("enter the number:");
scanf("%d",&search);
	
if(sequential_search(arr,search,size) == -1)
{
printf("Number %d not found in the arry.\n",search);
}
else
{
printf("Number %d found in the array at index %d.\n",search,sequential_search(arr,search,size));
}

return 0;
}
