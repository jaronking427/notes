#csci2270 
```cpp
int arr[] = {3,7};
int *p;
p = arr;

std::cout << *p << std::endl; //output: 3
//Pointer arithmatec
//Compiler casts the 1 to the correct number that will advance the memory address to the next byte
std::cout << *(p+1) << std::endl; //output: 6
//No longer pointer arithmetic 
std::cout << *p+1 << std::endl; //output: 4
//*p++ = *p+1
//*++p = *(p+1)
void myPBP(int * x);
void myPBA(int x[]);
//Interchangable for arrays
```
```cpp
void foo(int a, int &b, int *c, int d[]);
int main(){
	int x = 0, y = 0, *z, arr[];
	foo(x, y, z, arr);
	cout << x << ", " << y << endl;
}
void foo(int a, int &b, int *c, int d[]){
	cout << a << endl; //output: 0
	a = -28;
	b = -28; // Affects callers value
	c = nullptr;
	c = d; //Changing the pointer address c -> d -> arr[]
	*c = -1; //Works
}
```
```cpp
int * foo(){
	int *x;
	return x;
}
int * foo(){
	int x[] = {7,8,9,10};
	return x;
} //This will not work
```