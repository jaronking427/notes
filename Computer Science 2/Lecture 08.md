#csci2270 
## Pointer Arithmetic
```cpp
//Declare and initialize array
int arr[] = {3, 6};
//Set a pionter to point to the array
int *p = arr;
//Display the 0th element of the array using array syntax
std::cout << "Arr[0] " << arr[0] << std::endl;
//Use pointer syntax to print the first array element
std::cout << *p << std::endl;
//Display the 2nd element of the array
std::cout << arr[1] << std::endl;
//Display the 2nd element of the array
std::cout << *(p+1) << std::endl;
//Using the increment operator?
std::cout << *(++p) << std::endl; //NECESSARY TO USE PRE-INCREMENT
//Pre-increment increments p before dereferance
//Post-inerement dereferances and adds after dereferancing
std::cout << *(p++) << std::endl;
//Changes the memory address of p, now p points to 6 rather than 3
std::cout << ++(*p) << std::endl;
//Prints 6 + 1
```
## Memory
### Call Stack / Stack
- Local variables live on the call stack
- Automatic variables
- Once a function returns all of the local variables are no longer valid in the program
	- Does not immediately dissapear but other functions may write over the stack frame
	- Function is "popped" off of the stack
	- Returning pointers to local data in that function may lead to unpredictable results
- 
### Heap: Dynamic memory
```cpp
//CPP uses new/delete
int *p1 = new int;
*p1 = 7;
//Dealocate the var
delete p1;
```
