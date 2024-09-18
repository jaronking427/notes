#csci2270 
## Structs
- Primitive object
- All data is public
- No functions
```cpp
//Struct Example
struct Tree{
	string species;
	dobule height;
	bool deciduous;
	int number_branches;
	int length_each_branch[100];
}
```
```cpp
//Struct usage
int main(){
	Tree t0;
	t0.species = "juniper";
	t0.height = 24.5;
	t0.deciduous = false;
	t0.number_branches = 17;
	t0.length_each_branch[4] = 14;
}
```
## External file input
### How to read in external data files
1. Use the `<fstream>` library
2. Declare a stream object
3. Connect stream object the external file
4. Read in data until a delimiter is reached
5. Repeat step 4 until desired data has been read into your program
### Method A) assume white-space delimiter
```cpp
int x;
while(input_stream_object >> x){
	std::cout << x << std::endl;
}
```
### Method B) Custom delimiter
```cpp
std::string arr[10];
for(int i=0; i<10; i++){
	getline(myInStream, arr[i], ',');
}
```
