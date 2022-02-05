### dev：Visual Studio 2022
🕥2022年2月5日16:36:13
```C++
#include <iostream>
using namespace std;
int main() {
    //①array initialization:elementType arrayName[elementNumber];
    int nums1[3];
    nums1[0] = 1;
    nums1[1] = 2;
    nums1[2] = 3;
    cout << "①nums1: ";
    for (int i = 0; i < 3; i++) {
        cout << nums1[i] << " ";
    }
    //②array initialization:elementType arrayName[elementNumber] = {value1,value2,...};
    //If the number of values is inconsistent with the length of the array during initialization,data is zeroed out.
    int nums2[5] = {0,1,2,3};
    cout << endl << "②nums2: ";
    for (int i = 0; i < 3; i++) {
        cout << nums2[i] << " ";
    }
    //③array initialization:elementType arrayName[] = {value1,value2,...};
    //If no number of elements is specified,the size of the array is the number of elements at initialization.
    int nums3[] = { 0,1,2,3,4,5 };
    cout << endl << "③nums3: ";
    for (int i = 0; i < 6; i++) {
        cout << nums3[i] << " ";
    }
    cout << endl;
    cout << "The size of the entire array:" << sizeof(nums3) << endl;
    cout << "Each element takes up space:" << sizeof(nums3[0]) << endl;
    cout << "The number of elements in the array:" << sizeof(nums3) / sizeof(nums3[0]) << endl;

    cout << "Array header address:" << (int)nums3 << endl;
    cout << "The address of the first element in the array:" << (int)&nums3[0] << endl;
    cout << "The address of the second element in the array:" << (int)&nums3[1] << endl;
    return 0;
}
```
***控制台输出结果：***  

![image](https://user-images.githubusercontent.com/39286292/152644171-d274b5df-35e5-4bd9-aaed-9bf2febff412.png)
