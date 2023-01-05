# LinkedList-1
 Node* reverseList( Node* list)
{
    Node *prev = NULL, *cur = list, *next = NULL;
    while (cur != NULL) {
        next = cur->next;
        cur->next = prev;
        prev = cur;
        cur = next;
    }
    return prev;
}
 Node* addTwoLists(Node* first, Node* second)
{
    first = reverseList(first);
    second = reverseList(second);
 
    int carry = 0;
    Node *head = NULL, *prev = NULL;
    Node* sum = NULL;
    while (first != NULL || second != NULL || carry == 1)
    {
        int newVal = carry;
        if (first)
            newVal += first->data;
        if (second)
            newVal += second->data;
        carry = newVal / 10;
        newVal = newVal % 10;
        Node* newNode = new Node(newVal);
        newNode->next = sum;
        sum = newNode;
        if (first)
            first = first->next;
        if (second)
            second = second->next;
    }
 sum=reverse(sum);
    return sum;
}
