### dev：Visual Studio 2022
🕥2022年4月11日21:54:58
```C++
#include <iostream>
using namespace std;
//本质是在C++内部实现是一个指针常量
//发现是引用，转换为int* const ref = &a;
void func(int& ref) {
    ref = 100;//ref是引用，转换为*ref = 100;
}
int main() {
    int a = 10;

    //自动转换为int* const ref = &a;指针常量是指针指向不可更改，也说明了为什么引用不可更改
    int& ref = a;
    ref = 20;//ref是引用，转换为*ref = 100;
    cout << "a:" << a << endl;
    cout << "ref:" << ref << endl;
    func(a);
    cout << "a:" << a << endl;
    cout << "ref:" << ref << endl;
    return 0;
}
```
### Console output:
![image](https://user-images.githubusercontent.com/39286292/162755072-d0563425-deed-4351-9479-19e42d91daa9.png)
