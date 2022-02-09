### dev：Visual Studio 2022
🕥2022年2月3日21:30:44
```C++
#include <iostream>
using namespace std;
int main() {
    int a = 10;
    cout << !a << endl;
    cout << !!a << endl;
    int b = 1, c = 1;
    cout << (b && c) << endl;
    cout << (!b && c) << endl;
    cout << (b && !c) << endl;
    cout << (!b && !c) << endl;
    cout << (b || c) << endl;
    cout << (!b || c) << endl;
    cout << (b || !c) << endl;
    cout << (!b || !c) << endl;
    return 0;
}
```
***控制台输出结果：***  

![image](https://user-images.githubusercontent.com/39286292/152352728-322a8968-5a61-4dda-bba7-fe382a000a63.png)

