# LinkedList-1
Node *mergeTwoSortedLinkedLists(Node *head1, Node *head2){
    if(head1==NULL &&head2==NULL){
        return head1;
    }
    if(head1==NULL){
        return head2;

    }
    if(head2==NULL){
        return head1;
    }
    Node* fh; 
    Node*ft;
    if(head1->data< head2->data){
        fh=head1;
        ft=head1;
        head1=head1->next;
    }
    else{
        fh=head2;
        ft=head2;
        head2=head2->next;

    }
    while(head1!=NULL && head2!=NULL){
        if(head1->data<head2->data){
            ft->next=head1;
            ft=ft->next;
            head1=head1->next;
        }
        else{
            ft->next=head2;
            ft=ft->next;
            head2=head2->next;
        }

    }
    if(head1==NULL){
        ft->next=head2;
        return fh;
    }
    else{
        ft->next=head1;
return fh;
    }
}

