### dev：Visual Studio 2022
🕥2022年4月9日21:28:15
```C++
#include <iostream>
using namespace std;
//Value by pass
void swap1(int a, int b) {
	int temp = a;
	a = b;
	b = temp;
}
//Address by pass
void swap2(int* a, int* b) {
	int temp = *a;
	*a = *b;
	*b = temp;
}
//Reference by pass
void swap3(int& a, int& b) {
	int temp = a;
	a = b;
	b = temp;
}
int main() {
	int a = 10;
	int b = 20;

	swap1(a, b);
	cout << "a:" << a << " b:" << b << endl;

	swap2(&a, &b);
	cout << "a:" << a << " b:" << b << endl;

	swap3(a, b);
	cout << "a:" << a << " b:" << b << endl;
}
//引用与地址传递效果一致
```
### Console output:
![image](https://user-images.githubusercontent.com/39286292/162576150-12d70b5f-0415-4b0d-b3e8-aeec2e88a0e9.png)
