#csci2270 
## Queues
- "enqueue" at the "tail" of the queue
- "dequeue" from the head of the queue
- First in First out (FIFO)
- Examples
	- Printer
	- Call center
	- read/write commands in storage firmware 
	- wouldn't make sense to use for "Undo"
## Queue ADT 
```
private:
	head - the first item in the queue
	tail - last item in the queue ( or the index right after the last item)
	queue_size - number of elements currently in the queue
public:
	initialize()
	is_empty()
	is_full()
	enqueue(item) - add item to the end of the queue
	dequeue() - remove the top item from the queue
```
1. Linked list
2. Array
	a. linear 
	- Head is always element 0
	- tail holds index of next available element 
		- enQ(a)
		- enQ(b)
		- enQ(c)
	b. circular array queue implementation
	- 