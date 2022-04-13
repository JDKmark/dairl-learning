### dev：Visual Studio 2022
🕥2022年4月13日22:27:05
```C++
#include <iostream>
using namespace std;
int func(int a, int b = 10, int c = 10) {
    return a + b + c;
}
int func2(int a = 10, int b = 10);
int func2(int a, int b) {
    return a + b;
}
int main() {
    
    cout << "ret = " << func(100) << endl;
    cout << "ret = " << func(100,100,100) << endl;

    cout << "ret = " << func2() << endl;
    cout << "ret = " << func2(20, 20) << endl;
    return 0;
}
```
### Console output:
![image](https://user-images.githubusercontent.com/39286292/163203126-b35a8dc2-fd46-4f17-a5f1-c2079545eb02.png)
