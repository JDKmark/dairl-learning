### devï¼Visual Studio 2022
ð¥2022å¹´3æ28æ¥23:05:48

### æ¡ä¾æè¿°ï¼
è®¾è®¡ä¸ä¸ªè±éçç»æä½ï¼åæ¬æåå§åï¼å¹´é¾ï¼æ§å«;åå»ºç»æä½æ°ç»ï¼æ°ç»ä¸­å­æ¾5åè±éã

éè¿åæ³¡æåºçç®æ³ï¼å°æ°ç»ä¸­çè±éæç§å¹´é¾è¿è¡ååºæåºï¼æç»æå°æåºåçç»æã

äºåè±éä¿¡æ¯å¦ä¸ï¼
```C++
	{"åå¤",23,"ç·"},
	{"å³ç¾½",22,"ç·"},
	{"å¼ é£",20,"ç·"},
	{"èµµäº",21,"ç·"},
	{"è²è",19,"å¥³"},
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
        cout << "è±é åç§°:" << heros[i].name << " å¹´é¾:" << heros[i].age << " æ§å«:" << heros[i].sex << endl;
    }
}
int main() {
    Hero heros[5] = {
        {"åå¤",23,"ç·"},
        {"å³ç¾½",22,"ç·"},
        {"å¼ é£",20,"ç·"},
        {"èµµäº",21,"ç·"},
        {"è²è",19,"å¥³"}
    };
    int size = sizeof(heros) / sizeof(Hero);
    bubbleSort(heros, size);
    printHeros(heros, size);
    return 0;
}
```
### Console output:
![image](https://user-images.githubusercontent.com/39286292/160428639-155ab493-b364-4f1c-a36a-8f84c03ce143.png)
