# LinkedList-1
Node*insertnode(Node*head , int data){
	Node*temp=head;
	
Node*newNode=new Node(data);
head=newnode;
head->next=temp->next;
return head;

}
