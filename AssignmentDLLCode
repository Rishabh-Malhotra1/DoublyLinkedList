#include<bits/stdc++.h>
using namespace std;

struct node{
	node *front;
	node *prev;
	int num;
};


void InsertAtBegin(node **head,int n){
	
	node *ptr = new node();
	ptr->num = n;
	ptr->prev = NULL;
	if(*head==NULL){
		ptr->front = NULL;
		*head = ptr;
		return;
	}
	
	
	ptr->front = *head;
	(*head)->prev = ptr;
	*head = ptr;
}

void InsertAtEnd(node **head,int n){
	
	node *ptr = new node();
	ptr->num = n;
	ptr->front = NULL;
	if(*head==NULL){
		ptr->prev = NULL;
		*head = ptr;
		return;
	} 
	node *temp = new node();
	temp = *head;
	while(temp->front!=NULL){
		temp = temp->front;
	}
	temp->front = ptr;
	ptr->prev = temp;
	 
}
void DeleteAtEnd(node **head){
	if(*head==NULL){
		cout<<"List is empty";
		return;
	}
	if((*head)->front==NULL&&(*head)->prev==NULL){
		*head=NULL;
		return;
	}
	node *ptr = new node();
	ptr = *head;
	while(ptr->front!=NULL){
		ptr = ptr->front;
	}
	node *temp = new node();
	temp = ptr->prev;
	ptr->prev = NULL;
	temp->front = NULL;
	
	delete ptr;	
}

void DeleteAtBegin(node **head){
	if(*head==NULL){
		cout<<"List is Empty";
		return;
	}
	if((*head)->front==NULL&&(*head)->prev==NULL){
		*head=NULL;
		return;
	}
	node *ptr = new node();
	ptr = (*head)->front;
	(*head)->front->prev = NULL;
	ptr->prev = NULL;
	(*head)->front = NULL;
	node *temp = new node();
	temp = *head;
	delete temp;
	*head = ptr;
	
	
}

void Display(node *head){
	if(head==NULL){
		cout<<"List is Empty\n";
		return;
	}
	while(head!=NULL){
		cout<<head->num<<" ";
		head = head->front;
	}
	cout<<"\n";
}


node* Search(node *head,int n){
	if(head==NULL){
		return head;
	}
	while(head!=NULL){
		if(head->num==n){
			return head;
		}
		head = head->front;
	}
	return head;
}

int main(){
	
	node *head = new node();
	head = NULL;
	//Display(head);
	InsertAtBegin(&head,2312);
	InsertAtEnd(&head,1);
	InsertAtEnd(&head,23);
	InsertAtEnd(&head,1231);
	InsertAtEnd(&head,45);
	InsertAtEnd(&head,398);	
	DeleteAtEnd(&head);
	DeleteAtEnd(&head);
	DeleteAtBegin(&head);
	InsertAtBegin(&head,12);
	
	node *location1 = Search(head,1231);
	if(location1==NULL){
		cout<<"Not Found\n";
	}else{
		cout<<"Found\n";
	}
	location1 = Search(head,398);
	if(location1==NULL){
		cout<<"Not Found\n";
	}else{
		cout<<"Found\n";
	}
	Display(head);
			
}
