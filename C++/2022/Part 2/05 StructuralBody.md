### dev：Visual Studio 2022
🕥2022年3月21日22:55:59
```C++
#include <iostream>
using namespace std;
/*
Structure creation method
①struct structName variableName;
②struct structName variableName = { memberValue1,memberValue2,...};
③struct structName { 
    elementType structMember1;
    elementType structMember2;
    ....
}variableName;
*/

struct student {
    string name;
    int age;
    int score;
}stu3;
int main() {
    //Method 1
    struct student stu1;
    stu1.name = "张三";
    stu1.age = 18;
    stu1.score = 100;
    cout << "姓名： " << stu1.name << " 年龄： " << stu1.age << " 分数： " << stu1.score << endl;

    //Method 2
    struct student stu2 = { "李四",19,60 };
    cout << "姓名： " << stu2.name << " 年龄： " << stu2.age << " 分数： " << stu2.score << endl;

    //Method 3
    stu3.name = "王五";
    stu3.age = 18;
    stu3.score = 80;
    cout << "姓名： " << stu3.name << " 年龄： " << stu3.age << " 分数： " << stu3.score << endl;
    return 0;
}
```
### Console output:

![image](https://user-images.githubusercontent.com/39286292/159288355-38a028f8-437f-4af1-9feb-0bb1c8c13a30.png)
