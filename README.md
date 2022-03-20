# queue
#include<stdio.h>
#define MAX 6
int queue[MAX];
int rear=0,front=0;
void insert()
{
    int data;
        if(rear=MAX-1)
        {
                printf("liner quee is filled");
                return;
        }
        else
        {
                printf("enter the data");
                scanf("%d",&data);
                queue[rear]=data;
                rear++;
                printf("data is inserted in ques");
        }
}
void delete()
{
    int data;
        if(rear==front)
        {
                printf("quee is empty");
                return;
        }
        else
        {
                printf("enter the data");
                scanf("%d",&data);
                queue[rear]=data;
                rear++;
                printf("data is inserted in ques");
        }
}
void display()
{
        int i;
        printf("\n printing values is ...........\n");
        for(i=front;i<=rear;i++)
        {
                printf("%d",queue[i]);
        }
}
void main()
{
        int choice =0;
        while(choice<4)
        printf("operations on queue is");
        printf("enter 1-insert\n");
        printf("enter 2-delete\n");
        printf("enter 3-display\n");
        printf("enter your choice");
        scanf("%d",&choice);
        switch(choice)
        {
                case 1:
                        insert();
                        break;
                case 2:
                        delete();
                        break;
                case 3:
                        display();
                        break;
                default:
                        printf("wrong choice");
                        break;
        }
}
