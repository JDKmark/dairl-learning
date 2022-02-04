### dev：Visual Studio 2022
🕥2022年2月4日18:22:03
```C++
#include <iostream>
using namespace std;
int main() {
	for (int i = 0; i < 5; i++) {
		cout << i << endl;
	}
	for (int i = 1; i <= 50; i++) {
		if (i % 10 == 7 || i / 10 == 7 || i % 7 == 0) {
			cout << i << endl;
		}
	}
	return 0;
}
```
***控制台输出结果：***  

![image](https://user-images.githubusercontent.com/39286292/152513110-c0d75733-0d81-4339-bc7a-d9fcda456ce8.png)

