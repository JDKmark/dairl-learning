### dev：Visual Studio 2022
🕥2022年4月12日23:52:57
```C++
#include <iostream>
using namespace std;
void showValue(const int& value) {
    cout << value << endl;
}
int main() {
    const int& ref = 10;
    //warning: ref = 100;
    cout << ref << endl;

    //防止误操作修改实参
    int a = 10;
    showValue(a);
    return 0;
}
```
### Console output:
![image](https://user-images.githubusercontent.com/39286292/163003541-faf6f703-55dc-4b39-b58a-db33b7e24d35.png)
