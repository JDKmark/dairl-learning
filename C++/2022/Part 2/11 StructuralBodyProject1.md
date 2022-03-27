### dev：Visual Studio 2022
🕥2022年3月27日20:11:02

### 案例描述：

学校正在做毕设项目，每名老师带领5个学生，总共有3名老师，需求如下

设计学生和老师的结构体，其中在老师的结构体中，有老师姓名和一个存放5名学生的数组作为成员

学生的成员有姓名、考试分数，创建数组存放3名老师，通过函数给每个老师及所带的学生赋值

最终打印出老师数据以及老师所带的学生数据。
```C++
#include <iostream>
#include <ctime>
using namespace std;
struct Student {
    string name;
    int score;
};
struct Teacher {
    string name;
    Student stus[5];
};
void createData(Teacher teachers[], int num) {
    string teacherName = "老师";
    string studentName = "学生";
    string nameSeed = "ABCDE";
    for (int i = 0; i < num; i++) {
        teachers[i].name = teacherName + nameSeed[i];
        for (int j = 0; j < 5; j++) {
            teachers[i].stus[j].name = studentName + nameSeed[j];
            teachers[i].stus[j].score = rand()%101;
        }
    }
}
void printData(Teacher teachers[], int num) {
    for (int i = 0; i < num; i++) {
        cout << teachers[i].name << "老师的学生:" << endl;
        for (int j = 0; j < 5; j++) {
            cout << " 姓名:" << teachers[i].stus[j].name << " 成绩:" << teachers[i].stus[j].score << endl;
        }
    }
}
int main() {
    srand((unsigned int)time(NULL));
    Teacher teachers[3];
    int num = sizeof(teachers) / sizeof(Teacher);
    createData(teachers,num);
    printData(teachers, num);
    return 0;
}
```
### Console output:
![image](https://user-images.githubusercontent.com/39286292/160280792-1859d335-50f8-46bf-b5e6-b99cf0bab03d.png)
