### dev：Visual Studio 2022
🕥2022年2月13日23:09:44
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
void bubbleSort(int* arr, int len) {
    for (int i = 0; i < len - 1; i++) {
        for (int j = 0; j < len - i - 1; j++) {
            if (arr[j] > arr[j + 1]) {
                int temp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = temp;
            }
        }
    }
}
void printArray(int* arr, int len) {
    cout << "arr:";
    for (int i = 0; i < len; i++) {
        cout << arr[i] << " ";
    }
    cout << endl;
}
int main() {
    int a = 10, b = 5;
    cout << "a = " << a << " b = " << b << endl;
    swap1(a, b);
    cout << "After processing by swap1 function:a = " << a << " b = " << b << endl;
    swap2(&a, &b);
    cout << "After processing by swap2 function:a = " << a << " b = " << b << endl;
    int arr[] = { 7,5,4,1,8,9,3,2,6,0 };
    int len = sizeof(arr) / sizeof(arr[0]);
    printArray(arr, len);
    bubbleSort(arr, len);
    cout << "After processing by bubbleSort function.";
    printArray(arr, len);
    return 0;
}
```
### Console output:

![image](https://user-images.githubusercontent.com/39286292/153761100-cbc403f1-104c-4781-9dc6-3644b23d7158.png)
