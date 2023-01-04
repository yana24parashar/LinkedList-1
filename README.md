# LinkedList-1
Node*deletenode(Node*head){
	if(head==NULL){
		return head;
	}
Node*temp=head;
while(temp!=NULL){
	temp=temp->next;
}
if(temp!=NULL){
Node*a=temp->next;
Node*b;}
if(a){
b=a->next;}
else{
	b=NULL;
	temp->next=b;
	delete a;
}
return head;
}
