SinglyLinkedListNode* deleteNode(SinglyLinkedListNode* head, int position) {
 SinglyLinkedListNode *p,*q;

if(position==0){
    p=head;
    head=head->next;
    free(p);
}
else{
    p=head;    
  q=NULL;
    for(int i=0;i<position && p;i++){
        q=p;
        p=p->next;
    }
    q->next=p->next;
    free(p);
}
return head;

}

