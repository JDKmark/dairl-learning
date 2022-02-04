### dev：Visual Studio 2022
🕥2022年2月2日22:13:57
```C++
#include <iostream>
using namespace std;
int main() {
	int a = 10, b = 5, c = 0;
	c = a > b ? a : b;
	cout << "c = " << c << endl;

	//C++ 
	(a > b ? a : b) = 100;
	cout << "a = " << a << endl;
	cout << "b = " << b << endl;
	cout << "c = " << c << endl;
	return 0;
}
```
***控制台输出结果：***  

![image](https://user-images.githubusercontent.com/39286292/152475910-96c5d14d-4591-4786-9377-c73200868123.png)
