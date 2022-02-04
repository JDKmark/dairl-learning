### dev：Visual Studio 2022
🕥2022年2月4日15:08:06
```C++
#include <iostream>
using namespace std;
int main() {
	int num = 0;
	while (num < 5) {
		cout << num << endl;
		num++;
	}
	int guess = rand() % 100 + 1;
	int inputNum = 0;
	cout << "Now for the number game:" << endl;
	while (1) {
		cin >> inputNum;
		if (inputNum > guess) {
			cout << "Big" << endl;
		}
		else if(inputNum < guess) {
			cout << "Small" << endl;
		}
		else {
			cout << "Ok,The number is " << guess << endl;
		}
	}
	return 0;
}
```
***控制台输出结果：***  
1
![image](https://user-images.githubusercontent.com/39286292/152486719-cc792930-623e-4ab0-8537-4d61f8f2f849.png)
