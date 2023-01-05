# LinkedList-1
Node* mid(Node*head){
    Node* slow=head;
    Node*fast=head->next;
    while(fast!=NULL && fast->next!=NULL){
        fast=fast->next->next;
        slow=slow->next;
        
    }
    return slow;
}
Node* reverse(Node*head){
    is(head==NULL){
        return head;
    }
    Node*curr=head;
    Node*next=NULL;
    Node*prev=NULL;
    while(curr!=NULL){
        next=curr->next;
       curr->next=prev;
       prev=curr;
       curr=next;
    }
    return prev;
}

Node * foldll(Node* head){
    Node* c1 , *c2, *f1=NULL,*f2=NULL;
    Node*head1=head;
    Node*head2=mid(head);
    head2=reverse(mid->next);
    c1= head1; c2=head2, f1= c1->next; f2=c2->next;
    while(c2!=NULL){
        f1=c1->next;
        f2=c2->next;
        c1->next=c2;
        c2->next=f1;
        c1=f1;
        c2=f2;
        
    }
    
}
