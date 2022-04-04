### C++程序执行时，可将内存划分为4个区域
![image](https://user-images.githubusercontent.com/39286292/161436723-8b3f7321-d1f8-45f4-907c-7fdf88d45bf1.png)
### 程序运行前
![image](https://user-images.githubusercontent.com/39286292/161551934-e9d9fe6b-3857-472b-a1ef-e43116014429.png)
### 示例
```C++
#include <iostream>
using namespace std;
//global variable
int globalA = 10;
int globalB = 10;

//global constant
const int constantGlobalA = 10;
const int constantGlobalB = 10;

int main() {
    //local variable
    int a = 10;
    int b = 10;
     
    cout << "Local variable address:" << (int)&a << endl;
    cout << "Local variable address:" << (int)&b << endl;
    cout << "Global variable address:" << (int)&globalA << endl;
    cout << "Global variable address:" << (int)&globalB << endl;

    //static variable
    static int staticA = 10;
    static int staticB = 10;

    cout << "Static variable address:" << (int)&staticA << endl;
    cout << "Static variable address:" << (int)&staticB << endl;

    cout << "Constant variable address:" << (int)&"Hello World" << endl;
    cout << "Constant variable address:" << (int)&"Hello World1" << endl;

    cout << "Constant variable address:" << (int)&constantGlobalA << endl;
    cout << "Constant variable address:" << (int)&constantGlobalB << endl;

    //constant local variable
    const int constantLocalA = 10;
    const int constantLocalB = 10;
    cout << "Constant local variable address:" << (int)&constantLocalA << endl;
    cout << "Constant local variable address:" << (int)&constantLocalB << endl;
    return 0;
}
```
### 控制台输出
![image](https://user-images.githubusercontent.com/39286292/161555057-63010812-1c03-4841-854b-8d77a25a7f52.png)
