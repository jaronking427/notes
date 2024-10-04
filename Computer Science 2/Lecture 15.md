#csci2270 
## Algorithm Complexity
- A general way to compare algorithms 
- Performance
## Stack Data Structure
- Last in First out data structure
- A 'Limited access' Data structure 
	- Can only add to the top (push)
	- Can only remove from the top (pop)
- Usage examples:
	- Call stack
	- Undo stack in word editor
## STACK ADT
- private:
	- Top: top element
	- maxSize: limit of total size of the stack
	- Count: number of elements in stack
- Public:
	- Initialize() - constructor
	- bool isFull() - check whether stack is full
	- bool isEmpty() - check if the stack is empty
	- value peek() - show the top item
	- Push - add new item to the top
	- pop() remove from top  
	- disp() - print contents

```cpp
struct Node{
	std::string item;
	Node* next;
};
class Stack{
	private:
		Node *top;
		int count;
	public:
		Stack();
		~Stack();
		bool isEmpty();
		void push(std::string newItem);
		void pop();
		Node* peek();
		void disp();
};
```
```cpp
Stack::Stack(){
	count = 0;
	top = nullptr;
}
bool Stack::isEmpty(){
	if(top == nullptr){
		retrun true;
	}
		return false;
}
void Stack::push(std::string new_item){
	if(top == nullptr){
		top = new Node;
		top->item = new_item;
		top->next = nullptr;
	}
	else{
		Node* temp;
		temp = new Node;
		temp->item = new_item;
		temp->next = top;
		top = temp;
	}
}
void Stack::pop(){
	if(top == nullptr){
		return;
	}
	else{
		Node* new_top;
		new_top = top->next;
		delete top;
		top = new_top;
	}
}
Node* Stack::peek(){
	return top;
}
void Stack::disp(){
	Node* current_node;
	current_node = top;
	while(current_node != nullptr){
		std::cout << current_node->item << std::endl;
		current_node = current_node->next;
	}
}
```