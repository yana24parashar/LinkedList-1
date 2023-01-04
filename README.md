# LinkedList-1
Node*insertnode(Node*head , int data){
	Node*temp=head;
	if(head=NULL){
		Node *thisnode=new Node(data);
		head=thisnode;
		head->next=NULL;
		return head;}	
Node*newNode=new Node(data);
head=newnode;
head->next=temp->next;
return head;

}
