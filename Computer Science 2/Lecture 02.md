#csci2270
> git status
### Single file layout
```cpp
#include <iostream>
double foo(int x, string y); //Declaration

int main(){ //Every program needs main
	double z;
	z = foo(7,"hello");
	return 0;
}

double foo(int x, string y){ //Function definition
	cout << y << endl;
	reeturn x/2.0;
}
```
### Multi File Layout
```cpp
// Header file.hpp
double foo(int x, string y);
```
```cpp
// defs.cpp
#include <iostream>
#include "headerfile.hpp"

double foo(int x , string y){
	cout << y << endl;
	return x/2.0;
}
```
```cpp
//driver.cpp
#include <iostream>
#include "HeaderFile.hpp"
int main(){
	double z;
	z = foo(7, "hello");
	return 0;
}
```
> g++ std=c++11 driver.cpp defs.cpp
## Arrays
- Gets a data type, just like any variable
- C++ Arrays have to have a specified size
- The elements are contiguous in memory space 
	- Contiguous = "Elements on the array are back to back in the call stack"
```cpp
int arr[5];
arr[0] = 2270;
arr[6] = 12; //OUT OF BOUNDS
arr[2] = 1.9; //WRONG DATA TYPE!
```
