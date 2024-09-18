#csci2270 
# Review
```cpp
#include <iostream> 
#include <sstream>
#include <fstream>
//funciton prototypes 

//Read in file - 
//input arguments
// 1> array of strings
// 2> array length
// 3> name of text file
struct Student{
	int idNumber;
	std::string name;
	std::string dept;
};

void read_in_file(Student strArr[], int arrL, std::string file_name);

int main(int argc, char *argv[]){
	std::string file_name = "students.txt";
	int N = 10;
	Student student_array[10];
	//Function call
	readInFile(student_array, N, file_name);
	return 0;
}
void read_in_file(Student strArr[], int arrL, std::string file_name){
	std::ifstream input_file(file_name);
	std::string line, sid_string, student_name, student_department;
	if(!input_file.is_open()){
		std::cout << "Error" << std::endl;
		return;
	}
	getline(input_file, line);
	std::stringstream s(line);
	getline(s, sid_string, ',');
//Use a while loop instead
	for(int i=0; i<arrL; i++){
		getline(input_file, line);
		std::stringstream s(line);
		getline(s, sid_string, ',');
		strArr[i].idNumber = std::stoi(sid_string);
		getline(s, student_name, ',');
		stdArr[i].name = student_name;
		getline(s, student_department, ',');
		strArr[i].dept = student_department;		
	}
	input_file.close();
}
```
```
students.txt
444, Justine Henderson, Mechanical
933, Abdullah Lang, Aerospace
517, Marcus Cruz, Mechanical
262, Thalia Cobb, CompSci
ETC
```
# Pointers
A pointer is a variable that stores a memory address
## Important 
- We specify what data type is stored _at that_ address
- * used in declaration
## Notation
`int * p`
The above creates a pointer that points to an int the name of the pointer is p
- `*` specifies pointer type
	- `int * p` the asteriks in this case assigns a pointer
	- `*p = 7;` the asteriks in this case dereferances the pointer
- `&` address of operator
```cpp
double * ptr;
char * p0;
```
## Examples
```cpp
//Basic use of a pointer
int x; //Regular int variable
p = &x; //& is the address of operator
double y;
ptr = &y;
```
```cpp
//Using a pointer to access the original variable
int x;
p = &x;
*p = 7;
int z; 
z = *p; //the dereferance operation assigns z the value of the integer p is pointing to 
```
```cpp
std::cout << *p; // prints the value that the pointer is dereferancing 
std::cout << p; // prints the memory address that p is pointing to 
std::cout << &p; // prints the memory address of the pointer
```
# Pointer a a function parameter
```cpp 
//basic real use of a pointer
void foo(int * x);

int main(){
	int y = 8;
	int *p = &y;
	foo(p);
	cout << y;
	return 0;
}
void foo(int * x){
	*x = 0;
}
```
# Dereferancing 