### dev：Visual Studio 2022
🕥2022年2月6日15:37:26
```C++
#include <iostream>
using namespace std;
int main() {
    const int n = 6;
    int nums[n] = { 1,3,6,4,2,5 };
    cout << "Before ordering:" << endl;
    for (int i = 0; i < 6; i++) {
        cout << nums[i] << " ";
    }
    cout << endl;
    //①BubbleSort
    for (int i = 0; i < n - 1; i++) {
        for (int j = 0; j < n - i - 1; j++) {
            if (nums[j] > nums[j + 1]) {
                int temp = nums[j];
                nums[j] = nums[j + 1];
                nums[j + 1] = temp;
            }
        }
    }
    //②BubbleSort-Majorization
    bool flag;
    for (int i = 0; i < n - 1; i++) {
        flag = true;
        for (int j = 0; j < n - i - 1; j++) {
            if (nums[j] > nums[j + 1]) {
                int temp = nums[j];
                nums[j] = nums[j + 1];
                nums[j + 1] = temp;
                flag = false;
            }
            if (flag) {
                break;
            }
        }
    }
    cout << "After ordering:" << endl;
    for (int i = 0; i < 6; i++) {
        cout << nums[i] << " ";
    }
    cout << endl;
    return 0;;
}
```
***控制台输出结果：***  

![image](https://user-images.githubusercontent.com/39286292/152671761-fb972f43-feaa-4601-adb7-f5ab376d3835.png)
