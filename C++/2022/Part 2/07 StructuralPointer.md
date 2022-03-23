### dev：Visual Studio 2022
🕥2022年3月23日23:28:38
```C++
#include <iostream>
using namespace std;
struct student {
    string name;
    int age;
    int score;
};
int main() {
    struct student stu = { "张三",18,80 };
    struct student* p = &stu;
    p->score = 100;
    cout << "姓名： " << p->name << " 年龄： " << p->age << " 分数： " << p->score << endl;
    return 0;
}
```
### Console output:
![image](https://user-images.githubusercontent.com/39286292/159736197-1ab7c632-bb05-4d44-b617-b76c735a5a13.png)
