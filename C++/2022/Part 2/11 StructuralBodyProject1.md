### devï¼Visual Studio 2022
ð¥2022å¹´3æ27æ¥20:11:02

### æ¡ä¾æè¿°ï¼

å­¦æ ¡æ­£å¨åæ¯è®¾é¡¹ç®ï¼æ¯åèå¸å¸¦é¢5ä¸ªå­¦çï¼æ»å±æ3åèå¸ï¼éæ±å¦ä¸

è®¾è®¡å­¦çåèå¸çç»æä½ï¼å¶ä¸­å¨èå¸çç»æä½ä¸­ï¼æèå¸å§ååä¸ä¸ªå­æ¾5åå­¦ççæ°ç»ä½ä¸ºæå

å­¦ççæåæå§åãèè¯åæ°ï¼åå»ºæ°ç»å­æ¾3åèå¸ï¼éè¿å½æ°ç»æ¯ä¸ªèå¸åæå¸¦çå­¦çèµå¼

æç»æå°åºèå¸æ°æ®ä»¥åèå¸æå¸¦çå­¦çæ°æ®ã
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
    string teacherName = "èå¸";
    string studentName = "å­¦ç";
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
        cout << teachers[i].name << "èå¸çå­¦ç:" << endl;
        for (int j = 0; j < 5; j++) {
            cout << " å§å:" << teachers[i].stus[j].name << " æç»©:" << teachers[i].stus[j].score << endl;
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
