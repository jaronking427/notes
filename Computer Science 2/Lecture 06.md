#csci2270 
```cpp
//Pass by value
void myPBV(int x){
	x = -7;
}
int main(){
	int a = 2;
	cout << a << ", ";
	myPBV(a);
	cout << a << endl;
	//output 2, 2
}
```
```cpp
//Pass by referance 
void myPBR(int &x){
	x = -7;
}
//output 2, -7
//Ampersand allows a pass by referance 
//x becomes an alias of a
```
```cpp 
//Pass by pointer
void myPBP(int * x){
	//Passes memory address of a
	*x = -7; //Dereferance is necessary 
}
main(){
	int a = 2;
	int * p = &a;
	cout << a;
	myPBP(p);
	cout << a;
	//output 2, -7
}
```
```cpp
//Pass by array
void myPBA(int arr[]){
	arr[0] = -7;
}
int main(){
	 int arr[] = {5,6};
	 cout << arr[0];
	 myPBA(arr);
	 cout << arr[0];
}
```
```cpp
int arr[] = {3,6};
int * p;
p = arr;
//allowed
cout << p[0] << p[1];
int * p1 = {7,8};
```