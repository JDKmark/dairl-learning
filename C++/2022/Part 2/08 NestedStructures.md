### dev：Visual Studio 2022
🕥2022年3月24日22:24:17
```C++
#include  <iostream>
using namespace std;
struct student {
	string name;
	int age;
	int score;
};
struct teacher {
	int id;
	string name;
	int age;
	struct student stu;
};
int main() {
	struct teacher t1;
	t1.id = 10000;
	t1.name = "李老师";
	t1.age = 40;

	t1.stu.name = "张三";
	t1.stu.age = 18;
	t1.stu.score = 80;

	cout << "教师 职工编号: " << t1.id << " 姓名: " << t1.name << " 年龄: " << t1.age << endl;
	cout << "辅导学生 姓名: " << t1.stu.name << " 年龄: " << t1.stu.age << " 成绩: " << t1.stu.score << endl;

	return 0;
}
```
### Console output:
![image](https://user-images.githubusercontent.com/39286292/159937892-715731a1-8273-4e62-bfb9-7174b85a1c2e.png)
