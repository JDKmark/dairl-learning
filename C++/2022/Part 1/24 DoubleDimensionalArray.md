### dev：Visual Studio 2022
🕥2022年2月6日16:36:13
```C++
#include <iostream>
using namespace std;
int main() {
    //①Initialization of a double demensional array:elementType arrayName[RowCount][ColumnCount];
    int arr1[2][2];
    arr1[0][0] = 1;
    arr1[0][1] = 2;
    arr1[1][0] = 3;
    arr1[1][1] = 4;
    cout << "arr1:" << endl;
    for (int i = 0; i < 2; i++) {
        for (int j = 0; j < 2; j++) {
            cout << arr1[i][j] << " ";
        }
        cout << endl;
    }

    //②Initialization of a double demensional array:elementType arrayName[RowCount][ColumnCount]={{value1,value2,...},{value3,value4,...},...};
    int arr2[2][2] = { { 1 , 2 },{ 3 , 4 } };
    cout << "arr1:" << endl;
    for (int i = 0; i < 2; i++) {
        for (int j = 0; j < 2; j++) {
            cout << arr2[i][j] << " ";
        }
        cout << endl;
    }

    //③Initialization of a double demensional array:elementType arrayName[RowCount][ColumnCount] = {value1,value2,...};
    int arr3[2][2] = { 1,2,3,4 };
    cout << "arr1:" << endl;
    for (int i = 0; i < 2; i++) {
        for (int j = 0; j < 2; j++) {
            cout << arr3[i][j] << " ";
        }
        cout << endl;
    }

    //④Initialization of a double demensional array:elementType arrayName[][ColumnCount] = {value1,value2,...};
    int arr4[][2] = { 1,2,3,4 };
    cout << "arr1:" << endl;
    for (int i = 0; i < 2; i++) {
        for (int j = 0; j < 2; j++) {
            cout << arr4[i][j] << " ";
        }
        cout << endl;
    }

    cout << "The size of the entire array:" << sizeof(arr1) << endl;
    cout << "The size of a row in this array" << sizeof(arr1[0]) << endl;
    cout << "The size of the array element:" << sizeof(arr1[0][0]) << endl;

    cout << "The number of rows int this array:" << sizeof(arr1) / sizeof(arr1[0]) << endl;
    cout << "The number of columns in the array:" << sizeof(arr1[0]) / sizeof(arr1[0][0]) << endl;

    //address
    cout << "The first address of the array:" << arr1<< endl;
    cout << "The address of the first row of the array:" << arr1[0] << endl;
    cout << "The address of the second row of the array:" << arr1[0] << endl;

    cout << "The address of the first element of the array:" << &arr1[0][0] << endl;
    cout << "The address of the second element of the array:" << &arr1[0][1] << endl;
    return 0;
}
```
***控制台输出结果：***  

![image](https://user-images.githubusercontent.com/39286292/152682374-030db6b0-8ddf-4498-a748-1ff04f80eef3.png)

