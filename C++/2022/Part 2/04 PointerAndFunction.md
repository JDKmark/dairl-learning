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

![image](https://user-images.githubusercontent.com/39286292/153760324-5a5bcb0e-2c4f-4195-ae18-7294a09dc260.png)
