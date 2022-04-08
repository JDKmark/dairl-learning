### dev：Visual Studio 2022
🕥2022年4月8日22:38:53
```C++
#include <iostream>
using namespace std;
int main() {
	int a = 10;
	int& b = a;
	//warning: int &b;
	cout << "a = " << a << endl;
	cout << "b = " << b << endl;

	b = 99;
	
	cout << "a = " << a << endl;
	cout << "b = " << b << endl;

	int c = 10;
	int d = 20;
	int &e = c;
	e = d;//仅赋值，不改变引用
	cout << "c = " << c << endl;
	cout << "d = " << d << endl; 
	cout << "e = " << e << endl;

	return 0;
}
```
### Console output:
![image](https://user-images.githubusercontent.com/39286292/162460228-723974c7-4150-435b-b3a0-3ae2643c04ce.png)
