### dev：Visual Studio 2022
🕥2022年3月28日23:05:48

### 案例描述：
设计一个英雄的结构体，包括成员姓名，年龄，性别;创建结构体数组，数组中存放5名英雄。

通过冒泡排序的算法，将数组中的英雄按照年龄进行升序排序，最终打印排序后的结果。

五名英雄信息如下：
```C++
	{"刘备",23,"男"},
	{"关羽",22,"男"},
	{"张飞",20,"男"},
	{"赵云",21,"男"},
	{"貂蝉",19,"女"},
```

```C++
#include <iostream>
using namespace std;
struct Hero {
    string name;
    int age;
    string sex;
};
void bubbleSort(Hero heros[], int size) {
    for (int i = 0; i < size - 1; i++) {
        for (int j = 0; j < size - i - 1; j++) {
            if (heros[j].age > heros[j + 1].age) {
                Hero temp = heros[j];
                heros[j] = heros[j + 1];
                heros[j + 1] = temp;
            }
        }
    }
}
void printHeros(Hero heros[], int size) {
    for (int i = 0; i < size; i++) {
        cout << "英雄 名称:" << heros[i].name << " 年龄:" << heros[i].age << " 性别:" << heros[i].sex << endl;
    }
}
int main() {
    Hero heros[5] = {
        {"刘备",23,"男"},
        {"关羽",22,"男"},
        {"张飞",20,"男"},
        {"赵云",21,"男"},
        {"貂蝉",19,"女"}
    };
    int size = sizeof(heros) / sizeof(Hero);
    bubbleSort(heros, size);
    printHeros(heros, size);
    return 0;
}
```
### Console output:
![image](https://user-images.githubusercontent.com/39286292/160428639-155ab493-b364-4f1c-a36a-8f84c03ce143.png)
