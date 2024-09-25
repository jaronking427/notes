#csci2270 
## Linked List
```c
struct Node{
	int key;
	Node* next;
	
};
int main(){
	int arr[] = {5,12,14,17};
	N = 4;
	Node *head = malloc(sizeof(Node));
	Node *previous, *temp;
	head->key = arr[0];
	head->next = NULL;
	previous = head;
	for(int i=1; i<N; i++){
		temp = malloc(sizeof(Node));
		previous->next = temp;
		temp->key = arr[i];
		temp->next = NULL;
		previous = temp;
	}
	return 0;
}
```
