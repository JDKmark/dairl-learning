### dev：Visual Studio 2022
🕥2022年3月21日22:55:59
```C++
### dev：Visual Studio 2022
🕥2022年2月13日23:27:38
```C++
#include <iostream>
using namespace std;
//Pass by value
void swap1(int a, int b) {
    int temp = a;
    a = b;
    b = a;
}
//Pass by address
void swap2(int* a, int* b) {
    int temp = *a;
    *a = *b;
    *b = temp;
}
int main() {
    int a = 10, b = 5;
    cout << "a = " << a << " b = " << b << endl;
    swap1(a, b);
    cout << "After processing by swap1 function:a = " << a << " b = " << b << endl;
    swap2(&a, &b);
    cout << "After processing by swap2 function:a = " << a << " b = " << b << endl;
    return 0;
}
```
### Console output:

![image](https://user-images.githubusercontent.com/39286292/159288355-38a028f8-437f-4af1-9feb-0bb1c8c13a30.png)
