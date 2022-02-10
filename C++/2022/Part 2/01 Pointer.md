### dev：Visual Studio 2022
🕥2022年2月10日22:17:23
```C++
#include <iostream>
using namespace std;
int main() {
    int a = 10;
    int* p;
    p = &a;

    //The memory address of variable a
    cout << &a << endl;
    cout << p << endl;

    //Use of Pointers
    cout << "*p = " << *p << endl;

    cout << sizeof(p) << endl;
    cout << sizeof(char*) << endl;
    cout << sizeof(float*) << endl;
    cout << sizeof(double*) << endl;

    
    //Null pointer:Used to initialize a pointer
    /*
        The memory number starts from 0
        Memory 0 to 255 indicates the memory used by the ststem.
        Users are not allowed to access the memory.
        example:
            int *p1 = NULL;
            cout << *p1 << endl;

    */
    
    //Wild pointer:Pointer variables point to illegal memory space
    /*
        example:
            int* p2 = (int*)0x1100;
            cout << *p2 << endl;
    */
    return 0;
}
```
### Error caused by null and wild Pointers.  
![1644414425(1)](https://user-images.githubusercontent.com/39286292/153215889-3b4a152d-592d-45db-b510-a0015e1f47c2.png)

### Console output:
![image](https://user-images.githubusercontent.com/39286292/153426083-18b50d66-dfe2-4e86-9e40-6f6e9817a1ef.png)



