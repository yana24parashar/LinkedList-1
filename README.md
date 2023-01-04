# LinkedList-1
Node* insertNode(Node *head, int i, int data) {


if(head==NULL){
return head;

}

else if (i == 0) {
  Node *newNode = new Node(data);
 newNode->next=head;
 return newNode;


}
	Node*x= insertNode(head->next, i-1,data);
	head->next=x;
	return head;
  
}
