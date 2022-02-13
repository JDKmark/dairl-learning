### dev：Visual Studio 2022
🕥2022年2月13日23:09:44
```C++
#include <iostream>
using namespace std;
int main() {
	int arr[] = { 0,1,2,3,4,5,6,7,8,9 };
	int* p = arr;
	cout << "Access the first element: " << arr[0] << endl;
	cout << "Access the first element: " << *p << endl;
	
	//Through the array
	for (int i = 0; i < 10; i++) {
		cout << *p << " ";
		p++;
	}
	cout << endl;
	return 0;
}
```
### Console output:

![image](https://user-images.githubusercontent.com/39286292/153759647-e06d782f-5706-49f9-b510-1fff5d50157e.png)
