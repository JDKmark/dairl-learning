### dev：Visual Studio 2022
🕥2022年2月4日19:59:47
```C++
#include <iostream>
using namespace std;
int main() {
    //continue
    for (int i = 0; i < 5; i++) {
        if (i == 3) {
            cout << "continue" << endl;
            continue;
        }
        cout << i << endl;
    }
    //break;
    for (int i = 0; i < 10; i++) {
        for (int j = 0; j < 10; j++) {
            cout << "*";
            if (j == 4) {
                break;
            }
        }
        cout << endl;
        if (i == 4) {
            break;
        }
        
    }
    //goto
    cout << "A" << endl;
    cout << "B" << endl;
    goto FLAG;
    cout << "C" << endl;
    cout << "D" << endl;
    FLAG:
    cout << "E" << endl;
    return 0;
}
```
***控制台输出结果：***  

![image](https://user-images.githubusercontent.com/39286292/152525705-9a0ca690-d318-4f11-a414-d4c62b58e72a.png)

