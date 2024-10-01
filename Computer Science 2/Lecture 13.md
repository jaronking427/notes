#csci2270 
# Linked Lists
### Implementations in C++
Order of implementations 
1. Constructor
2. Search
3. Insert
4. Display 
5. Delete
```cpp
typedef struct node{
	int key; 
	node * next = NULL;
}
class SLL(){
	private:
	
	public:
	SLL::SLL(){
		node * head;
	}
	node* SLL::search(int sKey){
		node* crawler = head;
		while(crawler != nullptr && crawler->key != sKey){
			crawler = crawler->next;
		}
		return crawler;
	}
	void SLL:insert(int prevKey, int newKey){
		if(head == nullptr){
			head = new node;
			head->key = newKey;
		}
		else if(prevKey == -1){
			node* new_node = new node;
			new_node->key = newKey;
			new_node->next = head;
			head = new_node;
		}
		else{
			node* previous_node = search(prevKey);
			node* new_node;
			if(previous_node == nullptr){
				return;
			}
			new_node = new node;
			new_node->key = newKey;
			new_node->next = prevous_node->next;
			previous_node->next = new_node;	
		}
		return;
	}
}
```
