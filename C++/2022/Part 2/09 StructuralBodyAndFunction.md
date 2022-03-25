### dev：Visual Studio 2022
🕥2022年3月25日22:08:14
```C++
#include <iostream>
using namespace std;
struct student {
    string name;
    int age;
    int score;
};
//Pass by value
void printStudent(student stu) {
    stu.age = 28;
    cout << "子函数中 姓名: " << stu.name << " 年龄: " << stu.age << " 成绩: " << stu.score << endl;
}

//Pass by address
void printStudent2(student* stu) {
    stu->age = 28;
    cout << "子函数中 姓名: " << stu->name << " 年龄: " << stu->age << " 成绩: " << stu->score << endl;
}
int main() {
    student stu = { "张三",18,80 };

    //Pass by value
    printStudent(stu);
    cout << "主函数中 姓名: " << stu.name << " 年龄: " << stu.age << " 成绩: " << stu.score << endl;

    //Pass by value
    printStudent2(&stu);
    cout << "主函数中 姓名: " << stu.name << " 年龄: " << stu.age << " 成绩: " << stu.score << endl;

    return 0;
}
```
### Console output:
![image](https://user-images.githubusercontent.com/39286292/160136576-773ff19d-17de-47fa-b573-e18b0760e500.png)
