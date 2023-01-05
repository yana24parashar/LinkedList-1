# LinkedList-1
Node * Reverse(Node * head){
    if(head == nullptr){
        return nullptr;
    }
    Node * current = head;
    Node * next = NULL;
    Node * prev = NULL;
    while(current != NULL){
        next  = current->next;
        current->next = prev;
        prev = current;
        current = next;
    }
    return prev;
}
    

bool isPalindrome(Node *head)
{
    if (head == nullptr || head->next == nullptr){
        return true;
    }

    Node * front = head;
    Node * back = head->next;
    while(back != nullptr && back->next != nullptr ){
        front = front->next;
        back = back->next->next;
    }
    Node * mid = front;
   
    Node * newHead = mid->next;
    newHead = Reverse(newHead);
    
    Node * temp = head;
    Node * temp2 = newHead;
    
    while(temp != nullptr && temp2  != nullptr){
        if(temp->data == temp2->data){
            temp = temp->next;
            temp2 = temp2->next;
        }
        else{
            return false;
        }
    }
    
    return true;
}
