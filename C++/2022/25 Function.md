### dev：Visual Studio 2022
🕥2022年2月7日21:44:03
### ../源文件/25 Function.cpp
```C++
#include <iostream>
using namespace std;
#include "swap.h"
//The function structure 
/*
	elementType functionName(parameterList){
		code;
		return ;
	}
*/
//A function can be declared more than once,but a function can only be defined once.
int max(int a, int b);
int max(int a, int b);
int max(int a, int b) {
	return a > b ? a : b;
}
int add(int num1, int num2) {
	return num1 + num2;
}
//pass by value:When the function is called,the argument passes a value to the parameter.
int main() {
	int a = 10, b = 5;
	cout << "a + b = " << add(a, b) << endl;

	//pass by value
	swap(a,b);
	cout << "a:" << a << endl;
	cout << "b:" << b << endl;

	cout << "max(a,b)=" << max(a, b) << endl;
}
```
### ../头文件/swap.h
```C++
#include <iostream>
using namespace std;
void swap(int num1, int num2);
```

### ../源文件/swap.cpp
```C++
#include "swap.h"
void swap(int num1, int num2) {
	cout << "Exchange before:" << endl;
	cout << "num1:" << num1 << endl;
	cout << "num2:" << num2 << endl;
	int temp = num1;
	num1 = num2;
	num2 = temp;
	cout << "Exchange after:" << endl;
	cout << "num1:" << num1 << endl;
	cout << "num2:" << num2 << endl;
}

```
***控制台输出结果：***  

![image](https://user-images.githubusercontent.com/39286292/152799414-6a2a2db0-8ac7-4be4-a8f1-26f9c82bb999.png)


