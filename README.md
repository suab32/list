# list
#include <stdio.h>
#include <stdlib.h>
#include<limits.h>
struct node
{
	int data;
	struct node *next;
};
struct node *start=NULL;
void main()
{
	struct node *new;
	int val;
	int t=1,data;
	while(t)
	{
		new=(struct node *)malloc(sizeof(struct node));
		printf("Enter the value \n");
		scanf("%d",&data);
		create(new,data);
		printf("continue 1\n");
		scanf("%d",&t);
	}
	int *p=NULL;
	
		val=rev(p);
		printf("%d",val);

}

void create(struct node *new,int data)
{
	new->data=data;
	if(start==NULL)
	{
		start=new;
		new->next=NULL;
	}
	else
	{
		struct node *ptr;
		ptr=start;
		while(ptr->next!=NULL)
			ptr=ptr->next;
		ptr->next=new;
		new->next=NULL;

	}
}
 int rev(struct node *p)
{
	if(p==start)
		return(start->data);
	else
	{
		struct node *ptr;
		ptr=start;
		while(ptr->next!=p)
			ptr=ptr->next;
		retrun(rev(ptr));

	}
}
