# Hello-world
#include<stdio.h>
#define max 5
int deque[max];
int front;
int rear;
void enqueue_rear()
{
	int x;
	if((front==0&& rear==max-1)||(front==rear+1))
	{
		printf("Deque is overflow.\n");
		return ;
	}
	if(front==-1)
	{
		front=0;
		rear=0;
	}
	else if(rear==max-1)
	{
		rear=0;
	}
	else{
		rear=rear+1;
		printf("Enter the element you want to enqueue : ");
		scanf("%d",&x);
		deque[rear]=x;
	}	
}
void enqueue_front()
{
	int x;
	if((front==0 && rear==max-1)||(front==rear+1))
	{
		printf("Deque overflow !");
		return ;
	}
	if(front==-1)
	{
		front=0;
		rear=0;
	}
	else if(front==0){
		front=max-1;
	}
	else{
		front=front-1;
		printf("Enter the element you want to enqueue :");
		scanf("%d",&x);
		deque[front]=x;
	}
}
void dequeue_rear()
{
	if(front==-1)
	{
		printf("Deque underflow !");
		return ;
	}
	printf("Element dequeued from the deque is : %d",deque[rear]);
	if(front==rear)
	{
		front=-1;
		rear=-1;
	}
	else if(rear==0)
			rear=max-1;
		else
			rear=rear-1;	
}
void dequeue_front()
{
	if(front==-1)
	{
		printf("Deque Underflow !\n");
		return;
	}
	printf("Element dequeued from deque is %d",deque[front]);
	if(front==rear)
	{
		front=-1;
		rear=-1;
	}
	else
	{
		if(front==max-1)
		{
			front=0;
		}
		else{
			front=front+1;
		}
	}
}
void display_deque()
{
	int front1=front;
	int rear1=rear;
	if(front==-1)
	{
		printf("Deque is empty !\n");
		return ;
	}
	printf("Deque elements are : ");
	if(front1<=rear1)
	{
		while(front1<=rear1)
		{
			printf("%d",deque[front1]);
			front1++;
		}
	}
	else {
		while(front1<=max-1)
		{
			printf("%d",deque[front1]);
			front1++;
		}
		front1=0;
		while(front1<=rear1)
		{
			printf("%d",deque[front1]);
			front1++;
		}
	}
	printf("\n");
}
main()
{
	int choice,i=0;
	printf("1. Insert at rear.");
	printf("2. Insert at front.");
	printf("3. Delete from front.");
	printf("4. Delete from rear.");
	printf("5. display.");
	printf("6. Quit.");
	while(i==0)
	{
		switch(choice)
		{
			
		}
	}
}
