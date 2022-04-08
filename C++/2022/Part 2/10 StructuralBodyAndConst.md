### dev：Visual Studio 2022
🕥2022年3月26日22:16:04
```C++
#include <iostream>
using namespace std;
struct student {
	string name;
	int age;
	int score;
};
void printStudent(const student* stu) {
	//warn:stu->age = 80;
	cout << " 姓名: " << stu->name << " 年龄: " << stu->age << " 成绩: " << stu->score << endl;
}
int main() {
	student stu = { "张三",18,100 };
	printStudent(&stu);
	return 0;
}
```
### Console output:
![image](https://user-images.githubusercontent.com/39286292/160243524-ab51a062-2b6c-4351-9891-6a764944dbaf.png)
