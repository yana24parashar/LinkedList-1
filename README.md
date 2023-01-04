# LinkedList-1
int kfromlast(Node*head , k){
Node*s=head;
Node*f=head;
for(inti=0; i<k ; i++){
f=f->next;}
while(f!=NULL){
s=s->next;
f=f->next;}
return s->data;}
