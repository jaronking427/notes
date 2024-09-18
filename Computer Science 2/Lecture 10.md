#csci2270 

```cpp
void foo(int a_foo[]){
	cout << "C > " << a_foo << std::endl; //Prints the same memory address of the pointer
	std::cout << "D > " << &a_foo << std::endl; //Prints a uniqe address because a copy is made in the function call 
}
int main(){
	int n = 3;
	int *a_main = new int[n];

	std::cout << "A> " << a_main << std::nedl; //Prints memory address of pointer
	cout << "B > " << &a_main << std::endl; //Prints the pointee memeory address
	foo(a_main);
	return 0;
}
```
```cpp
void foo(int *& a_foo[]){
	cout << "C > " << a_foo << std::endl; //Prints the same memory address of the pointer
	std::cout << "D > " << &a_foo << std::endl; //Prints the same address as b
}
int main(){
	int n = 3;
	int *a_main = new int[n];

	std::cout << "A> " << a_main << std::nedl; //Prints memory address of pointer
	cout << "B > " << &a_main << std::endl; //Prints the pointee memeory address
	foo(a_main);
	return 0;
}
```
## Pointers to structs 
```cpp
struct Student{
	std::string name;
	int age;
};
int main(){
	Student s0, s1;
	Student * sptr = new Student;
	sptr->name = "";
	sptr->age = 19;
	(*sptr).name = "Pat";
	(*sptr).age = 44;
}
```
```cpp

```