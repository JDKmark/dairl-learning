### dev：Visual Studio 2022
🕥2022年2月4日18:22:03
```C++
#include <iostream>
using namespace std;
int main() {
    for (int i = 0; i < 5; i++) {
        cout << i << endl;
    }
	//10*10的星星图
    for (int i = 0; i < 10; i++) {
        for (int j = 0; j < 10; j++) {
            cout << "*";
        }
        cout << endl;
    }
	//九九乘法表
    for (int i = 1; i < 10; i++) {
        for (int j = 1; j <= i; j++) {
            cout << i << " * " << j << " = " << i * j << " ";
        }
        cout << endl;
    }
    return 0;
}
```
***控制台输出结果：***  

![image](https://user-images.githubusercontent.com/39286292/152513779-a00a5df4-ec97-4ec2-8568-9f942217d231.png)

