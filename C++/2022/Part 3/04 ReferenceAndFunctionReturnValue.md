### dev：Visual Studio 2022
🕥2022年4月10日22:11:33
```C++
#include <iostream>
using namespace std;
int& test1() {
    int a = 10;
    return a;
}
int& test2() {
    static int a = 10;
    return a;
}
int main() {
    int& ref = test1();
    cout << "ref = " << ref << endl;
    cout << "ref = " << ref << endl;

    int& ref2 = test2();
    cout << "ref2 = " << ref2 << endl;
    cout << "ref2 = " << ref2 << endl;

    test2() = 1000;
    cout << "ref2 = " << ref2 << endl;
    cout << "ref2 = " << ref2 << endl;

    return 0;
}
```
### Console output:
![image](https://user-images.githubusercontent.com/39286292/162623481-5c577e2c-407f-471c-a14e-a9b1c3253d74.png)
