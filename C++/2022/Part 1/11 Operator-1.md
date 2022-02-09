### dev：Visual Studio 2022
🕥2022年2月1日22:31:57
```C++
#include <iostream>
using namespace std;
int main() {
    int a = 10, b = 5;
    cout << "a + b = " << a + b << endl;
    cout << "a - b = " << a - b << endl;
    cout << "a * b = " << a * b << endl;
    cout << "a / b = " << a / b << endl;
    cout << "a % b = " << a % b << endl;
    a = 2,b = a++;
    cout << "a = " << a << " b = " << b << endl;
    a = 2, b = ++a;
    cout << "a = " << a << " b = " << b << endl;
    a = 2, b = a--;
    cout << "a = " << a << " b = " << b << endl;
    a = 2, b = --a;
    cout << "a = " << a << " b = " << b << endl;
    return 0;
}
```
***控制台输出结果：***  

![image](https://user-images.githubusercontent.com/39286292/151988379-a748a6db-4ff9-4ffa-bf2a-2298f99ac334.png)
