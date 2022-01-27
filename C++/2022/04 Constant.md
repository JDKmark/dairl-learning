### dev：Visual Studio 2022
🕥2022年1月27日21:32:41
```C++
#include <iostream>
using namespace std;
#define month 12
int main() {
	const int week = 7;
	cout << "one year=" << month << endl;
	//month = 9; 报错：不能给常量赋值
	cout << "one week=" << week << endl;
	//week = 9; 报错：不能给常量赋值
	system("pause");
	return 0;
}
```
