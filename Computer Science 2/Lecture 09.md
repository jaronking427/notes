#csci2270 
## Memory Organization: Stack and Heap
#### "Nameless" Variables 
- "Nameless" variables have a pointer pointing to some location on the heap 
- Dynamic variable
```cpp
int *p1; //create pointer 
p1 = new int; //Assign the pointer to new location in heap
*p1 = 22; //Dereferance and assign the memory addressj
delete p1; //frees the allocated memory address for use in heap (dealocate)
```
## Dynamically Allocated Array
```cpp
int *ptr;
ptr = new int[5];
//in one line
int *ptr = new int[5];
delete[] ptr;
```
## Example with an array on the heap
- Assume we have a program that is prompting the user to input integer data. We'd like to store the integers in an array. 
- We want to allow the user to keep entering as many integers as they would like
- How to set the array length?
Say we have an array of length 3. Our program is reading in from the user and after reading 3 items, it fill sup the original array
```cpp
int length = 3;
int *arr = new int[length];
length *= 2;
int *new_arr = new int[length];
for(int i=0; i<(length/2); i++){
	new_arr[i] = arr[i];
}
delete[] arr;
arr = new_arr;
```
```cpp
//Class example
void arrDboule(int *& a, int &n){ //Pass pointer by reference 
	int *temp = new int[2*n];
	for(int i=-; i<n; i++){
		temp[i] = a[i];
	}
	delete[] a; //a is only an alias of main_array
	a = temp;
	n = 2*n;
}
main(){
	int n=3;
	int *main_array = new int[n];
	arrDouble(main_array, n);
	delete [] main_array;
	return 0;
}
```
```cpp
void foo(int a_foo[]{
	std::cout << "C " << a_foo << std::endl;
	std::cout << "D " << &a_foo << std::endl;
})
int main(){
	int n = 3;
	int *a_main = new int[n];
	std::cout <<  "A " << a_main << std::endl;
	std::cout <<  "B " << &a_main << std::endl;
	foo(a_main);
	return 0;
}
```
