### dev：Visual Studio 2022
🕥2022年2月4日13:58:54
```C++
#include <iostream>
using namespace std;
int main() {
    int score = 0;
    cout << "Please enter a number(0<=number<=5):" << endl;
    cin >> score;
    switch (score) {
        case 5:
            cout << "A" << endl;
            break;
        case 4:
            cout << "B" << endl;
            break;
        case 3:
            cout << "C" << endl;
            break;
        case 2:
            cout << "D" << endl;
            break;
        case 1:
            cout << "E" << endl;
            break;
        default:
            cout << "F" << endl;
            break;
    }

    return 0;
}
```
