# LinkedList-1
Node *midPoint(Node *head) {
  Node *slow = head, *fast = head->next;
  while (fast != NULL && fast->next != NULL) {
    fast = fast->next->next;
    slow = slow->next;
  }
  return slow;
}
//sorted merging
Node *mergesortedll(Node* head1 , Node* head2){
  if(head1==NULL){
    return head2;
  }
  else if(head2==NULL){
    return head1;
  }
  Node* fh;
  Node*ft;
if(head1->data<head2->data){
  fh=ft=head1;
  head1=head1->next;
}
else{
  fh=ft=head2;
  head2=head2->next;

}
while(head1 !=NULL && head2!=NULL){
  if(head1->data<head2->data){
 
    ft->next=head1;
    ft=ft->next;
    head1=head1->next;
  }
  else {

ft->next=head2;
ft=ft->next;
head2=head2->next;
  }

}
if(head1==  NULL){
  ft->next=head2;
}
else {
  ft->next= head1;
}
return fh;
}
Node *mergeSort(Node *head){
  if(head==NULL || head->next==NULL){
    return head;
  }
  Node* mid= midPoint(head);
  Node*h1=head;
  Node*h2=mid->next;
  mid->next=NULL;
  h1= mergeSort(h1);
  h2=mergeSort(h2);
  Node* finalsub= mergesortedll(h1 , h2);
  return finalsub;
}
