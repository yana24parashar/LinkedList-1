# LinkedList-1

void reversell( Node*head){
if(head==NULL){
return;}
Node*x=reversell(head->next);
x->next=head;
return x;}
