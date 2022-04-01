### dev：Visual Studio 2022
🕥2022年4月1日23:25:17

### 案例描述：
通讯录是一个可以记录亲人、好友信息的工具。

本教程主要利用C++来实现一个通讯录管理系统

系统中需要实现的功能如下：

* 添加联系人：向通讯录中添加新人，信息包括（姓名、性别、年龄、联系电话、家庭住址）最多记录1000人
* 显示联系人：显示通讯录中所有联系人信息
* 删除联系人：按照姓名进行删除指定联系人
* 查找联系人：按照姓名查看指定联系人信息
* 修改联系人：按照姓名重新修改指定联系人
* 清空联系人：清空通讯录中所有信息
* 退出通讯录：退出当前使用的通讯录

### 代码实现
```C++
#include <iostream>
#include <string>
#include<iomanip>
using namespace std;
#define MAX 1000
struct People {
    string name;
    string sex;
    int age;
    string phone;
    string address;
};
struct AddressBook {
    struct People peoples[MAX];
    int size;
};
void showMenu() {
    cout << "******************************" << endl;
    cout << "*********1.添加联系人*********" << endl;
    cout << "*********2.显示联系人*********" << endl;
    cout << "*********3.删除联系人*********" << endl;
    cout << "*********4.查找联系人*********" << endl;
    cout << "*********5.修改联系人*********" << endl;
    cout << "*********6.清空联系人*********" << endl;
    cout << "*********0.退出通讯录*********" << endl;
    cout << "******************************" << endl;
}
void addPerson(AddressBook *addressBook) {
    if (addressBook->size >= MAX) {
        cout << "不好意思，通讯录已满" << endl;
        return;
    }
    else {
        string name, sex, phone, address;
        int age = 0;
        cout << "请输入姓名:" << endl;
        cin >> name;

        cout << "请输入性别(男/女):" << endl;
        cin >> sex;

        cout << "请输入年龄:" << endl;
        cin >> age;

        cout << "请输入电话:" << endl;
        cin >> phone;

        cout << "请输入地址:" << endl;
        cin >> address;
        addressBook->peoples[addressBook->size].name = name;
        addressBook->peoples[addressBook->size].sex = sex;
        addressBook->peoples[addressBook->size].age = age;
        addressBook->peoples[addressBook->size].phone = phone;
        addressBook->peoples[addressBook->size].address = address;
        addressBook->size++;
        cout << "添加联系人" << name << "成功" << endl;
        system("pause");
        system("cls");
    }

}
void showAddressBoos(AddressBook* addressBook) {
    cout << left << setw(12) << "姓名" << std::left << setw(12) << "性别" << std::left << setw(12)<<"年龄" << std::left << setw(12)<<"电话" << std::left << setw(12)<<"地址" << endl;
    for (int i = 0; i < addressBook->size; i++) {
        cout << std::left << setw(12) << addressBook->peoples[i].name;
        cout << std::left << setw(12) << addressBook->peoples[i].sex;
        cout << std::left << setw(12) << addressBook->peoples[i].age;
        cout << std::left << setw(12) << addressBook->peoples[i].phone;
        cout << std::left << setw(12) << addressBook->peoples[i].address <<  endl;
    }
    system("pause");
    system("cls");
}
int isExist(AddressBook* addressBook, string name) {
    for (int i = 0; i < addressBook->size; i++) {
        if (addressBook->peoples[i].name == name) {
            return i;
        }
    }
    return -1;
}
void deletePersion(AddressBook* addressBook) {
    string name;
    cout << "请输入删除的联系人姓名:" << endl;
    cin >> name;
    int index = isExist(addressBook, name);
    if (index != -1) {
        for (int i = index; i < addressBook->size - 1; i++) {
            addressBook->peoples[i] = addressBook->peoples[i + 1];
        }
        addressBook->size--;
        cout << "删除联系人" << name << "成功" << endl;
    }
    else {
        cout << "查无此人" << endl;
    }
    system("pause");
    system("cls");
}
void searchPerson(AddressBook* addressBook) {
    string name;
    cout << "请输入查找的联系人姓名:" << endl;
    cin >> name;
    int index = isExist(addressBook, name);
    if (index != -1) {
        cout << "姓名:" << addressBook->peoples[index].name;
        cout << " 性别:" << addressBook->peoples[index].sex;
        cout << " 年龄:" << addressBook->peoples[index].age;
        cout << " 电话:" << addressBook->peoples[index].phone;
        cout << " 地址:" << addressBook->peoples[index].address << endl;
        cout << "查询成功！" << endl;
    }
    else {
        cout << "查无此人" << endl;
    }
    system("pause");
    system("cls");
}
void changePerson(AddressBook* addressBook) {
    string nowName;
    cout << "请输入修改的联系人姓名:" << endl;
    cin >> nowName;
    int index = isExist(addressBook, nowName);
    if (index != -1) {
        string name, sex, phone, address;
        int age = 0;

        cout << "请输入姓名:" << endl;
        cin >> name;

        cout << "请输入性别(男/女):" << endl;
        cin >> sex;

        cout << "请输入年龄:" << endl;
        cin >> age;

        cout << "请输入电话:" << endl;
        cin >> phone;

        cout << "请输入地址:" << endl;
        addressBook->peoples[index].name = name;
        addressBook->peoples[index].sex = sex;
        addressBook->peoples[index].age = age;
        addressBook->peoples[index].phone = phone;
        addressBook->peoples[index].address = address;
        cout << "修改成功！" << endl;
    }
    else {
        cout << "查无此人" << endl;
    }
    system("pause");
    system("cls");
}
void clearAddressBook(AddressBook* addressBook) {
    addressBook->size = 0;
    cout << "已清空通讯录！" << endl;
    system("pause");
    system("cls");
}
int main() {
    int select = 0;
    AddressBook addressBook;
    addressBook.size = 0;
    while (true) {
        showMenu();
        cin >> select;
        switch (select)
        {
            case 1:
                addPerson(&addressBook);
                break;
            case 2:
                showAddressBoos(&addressBook);
                break;
            case 3:
                deletePersion(&addressBook);
                break;
            case 4:
                searchPerson(&addressBook);
                break;
            case 5:
                changePerson(&addressBook);
                break;
            case 6:
                clearAddressBook(&addressBook);
                break;
            case 0:
                cout << "欢迎下次使用" << endl;
                return 0;
                break;
            default:
                break;
        }
    }
    return 0;
}
```
### 控制台输出:
![image](https://user-images.githubusercontent.com/39286292/161294392-b4f81f3e-7d1e-442d-a9ea-b0cf954778e2.png)
![image](https://user-images.githubusercontent.com/39286292/161294527-a3485b4e-02b4-4846-afd9-e8bf031f8f11.png)
![image](https://user-images.githubusercontent.com/39286292/161294592-fc55d194-abd6-4808-ab77-ceee75860f08.png)
![image](https://user-images.githubusercontent.com/39286292/161294656-251240fd-a8c9-4c40-9dab-038f0046dee6.png)



