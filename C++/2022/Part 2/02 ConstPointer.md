### dev：Visual Studio 2022
🕥2022年2月10日22:34:23
```C++
#include <iostream>
int main() {
	int a = 10;
	int b = 5;

	//The variable pointed to by pointer P1 can be changed,but the value pointed to by pointer P1 cannot be changed.
	const int* p1 = &a;
	p1 = &b;//Yes
	//No:*p1 = 100;

	//The value pointed to by pointer P2 can be changed,but the variable pointed to by pointer P1 cannot be changed.
	int* const p2 = &a;
	*p2 = 100;//Yes
	//No:p2 = &b;

	//The variable and value to which the pointer P1 points cannot be changed.
	const int* const p3 = &a;
	/*
		No:p3 = &b;*p3 = 100;
	*/
	return 0;
}
```
