### dev：Visual Studio 2022
🕥2022年3月22日23:48:44
```C++
/*
StructuralArray
struct structName arrayName[elementNum] = { {},{},...};
*/
#include <iostream>
using namespace std;
struct student {
 string name;
 int age;
 int score;
};
int main(){
 struct student arr[3] = {
  {"张三",18,60},
  {"李四",19,60},
  {"王五",20,70}
 };
 for (int i = 0; i < 3; i++) {
  cout << "姓名： " << arr[i].name << " 年龄： " << arr[i].age << " 分数： " << arr[i].score << endl;
 }
 return 0;
}
```
### Console output:
![image](https://user-images.githubusercontent.com/39286292/159523000-b468d01a-c5dc-4e3c-933d-780229809588.png)
