#csci2270 
## Memory (RAM)
1. Code Text
	1. Instructions
2. Static Global
	1. Global variables/ whole lifetime of runtime
3. Local variables/funciton calls
	1. Stays alive as long as the funciton is running 
4. Heap
	1. Dynamic memory
First three are fixed size, predetermined at runtime, but the last one is dynamic
### Applications memory
```c
#include<stdio.h>
//Total variable goes in static because it is global
int total;
int square(int x){
	return x*x;
}
int squareOfSum(int x, int y){
	//Data stored in stack
	int z = square(x+y);
	return z;
}
//Each function is in its own stack frame
int main(){
	//All variables in the funciton are stored in stack
	int a = 4; 
	int b = 8;
	total = squareofsum(a,b); //Stack is populated at this moment
	printf("output = %d", total);
}
```
> Memory stacks on top of itself
> Other functions pause as the top funciton is ran and it is ran through the top down
### Pointer
| Address | Value |
| ------- | ----- |
| 139     | 4     |
| 140     | 139   |
|         |       |
```c
int x = 4; // Address of x is 139
int *px = &x; //Holds value memory address 139
```
### Heap
```c
#include<stdio.h>
#include<stdlib.h>
int main(){
	int a;
	int *p;
	p = new int;
	*p = 10;
	delete p;
	p = new int[20];
	delete[] p;
}
```
### Structs
```cpp
Struct Student{
	int age;
	std::string name;
	int id;
	float gpa;
	bool enrolled;	
}
Student leo{20, "Leo", 123456, 3.9, True};
```