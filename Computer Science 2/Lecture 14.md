#csci2270
## Destructor 
Needed for dynamic memory
- Gets called automatically like the constructor
- Called when the class gets popped off the call stack
- Can be called manually, but it is unconventional 
- Prevents memory leaks
```cpp
int main(){
	SLL s0;
	s0.~SLL(); //Unconventional not typically used
}
```
```cpp
SLL::~SLL(){
	Node* crawler;
	while(head!=nullptr){
		crawler = head;
		head = crawler->next;
		delete crawler;
	}
}
```

