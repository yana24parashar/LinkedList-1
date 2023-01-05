# LinkedList-1
int getcount(Node*head){
int count=0;
Node*temp=head;
while(temp!=NULL){
temp=temp->next;
count++;}
return count;}


int_getd(Node*head1 , Node*head2){
int d;
int m= getcount(head1);
int n=getcount(head2);
if(m>n){
 d=m-n;
return getIntersectionNode(d , head1, head2);
else
int d= n-m;
return getIntersection(d , head2, head1);}

int _getIntesectionNode(int d, Node* head1, Node* head2)
{
    Node* current1 = head1;
    Node* current2 = head2;
    for (int i = 0; i < d; i++) {
        current1 = current1->next;
    }

    while (current1 != NULL && current2 != NULL) {
        if (current1 == current2)
            return current1->data;}

        current1 = current1->next;
        current2 = current2->next;
    }
 
    return -1;
}
