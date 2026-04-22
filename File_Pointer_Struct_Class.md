# 🚀 C++ Nâng Cao Cơ Bản – File, Pointer, Struct, Class

---

# 📂 1. XỬ LÝ FILE

## 🧠 Thư viện

```cpp
#include <fstream>
```

---

## 🔹 Ghi file

```cpp
#include <iostream>
#include <fstream>
using namespace std;

int main() {
    ofstream file("data.txt");

    file << "Hello File";
    file.close();
}
```

---

## 🔹 Đọc file

```cpp
#include <iostream>
#include <fstream>
using namespace std;

int main() {
    ifstream file("data.txt");
    string line;

    while (getline(file, line)) {
        cout << line << endl;
    }

    file.close();
}
```

---

## 🔹 Kiểm tra file mở thành công

```cpp
ifstream file("data.txt");
if (!file) {
    cout << "Mo file that bai";
}
```

---

## 🔹 Ghi thêm (append)

```cpp
ofstream file("data.txt", ios::app);
```

---

# 🧪 BÀI TẬP FILE

---

## 🟢 Bài 1: Ghi số vào file

### Đề

Nhập n, ghi từ 1 → n vào file

### Đáp án

```cpp
#include <iostream>
#include <fstream>
using namespace std;

int main() {
    int n;
    cin >> n;

    ofstream file("numbers.txt");

    for (int i = 1; i <= n; i++) {
        file << i << " ";
    }

    file.close();
}
```

---

## 🟡 Bài 2: Đọc file và tính tổng

### Đề

Đọc các số trong file, tính tổng

### Đáp án

```cpp
#include <iostream>
#include <fstream>
using namespace std;

int main() {
    ifstream file("numbers.txt");

    int x, sum = 0;
    while (file >> x) {
        sum += x;
    }

    cout << sum;
}
```

---

# 👉 2. CON TRỎ (POINTER)

## 🧠 Khái niệm

* Pointer lưu địa chỉ bộ nhớ

---

## 🔹 Khai báo

```cpp
int a = 10;
int* p = &a;
```

---

## 🔹 Truy cập giá trị

```cpp
cout << *p;  // 10
```

---

## 🔹 Thay đổi giá trị

```cpp
*p = 20;
```

---

## 🔹 Pointer NULL

```cpp
int* p = nullptr;
```

---

## 🔹 Pointer với mảng

```cpp
int arr[3] = {1,2,3};
int* p = arr;

cout << *(p + 1); // 2
```

---

# 🧪 BÀI TẬP POINTER

---

## 🟢 Bài 3: Đổi giá trị qua pointer

```cpp
#include <iostream>
using namespace std;

void update(int* p) {
    *p = 100;
}

int main() {
    int a = 5;
    update(&a);
    cout << a;
}
```

---

## 🟡 Bài 4: Hoán đổi 2 số

```cpp
#include <iostream>
using namespace std;

void swapNum(int* a, int* b) {
    int temp = *a;
    *a = *b;
    *b = temp;
}

int main() {
    int x = 3, y = 7;
    swapNum(&x, &y);
    cout << x << " " << y;
}
```

---

# 🧱 3. STRUCT

## 🔹 Khai báo

```cpp
struct Student {
    string name;
    int age;
};
```

---

## 🔹 Sử dụng

```cpp
Student s;
s.name = "Vu";
s.age = 22;
```

---

## 🔹 Mảng struct

```cpp
Student arr[100];
```

---

# 🧪 BÀI TẬP STRUCT

---

## 🟢 Bài 5: Nhập & in sinh viên

```cpp
#include <iostream>
using namespace std;

struct Student {
    string name;
    int age;
};

int main() {
    Student s;

    cin >> s.name >> s.age;

    cout << s.name << " " << s.age;
}
```

---

# 🏗️ 4. CLASS

## 🔹 Khai báo

```cpp
class Student {
public:
    string name;
    int age;

    void show() {
        cout << name << " " << age;
    }
};
```

---

## 🔹 Sử dụng

```cpp
Student s;
s.name = "Vu";
s.age = 22;
s.show();
```

---

## 🔹 Constructor

```cpp
class Student {
public:
    string name;

    Student(string n) {
        name = n;
    }
};
```

---

# 🧪 BÀI TẬP CLASS

---

## 🔵 Bài 6: Tạo class + method

```cpp
#include <iostream>
using namespace std;

class Rectangle {
public:
    int w, h;

    int area() {
        return w * h;
    }
};

int main() {
    Rectangle r;
    r.w = 5;
    r.h = 10;

    cout << r.area();
}
```

---

# 🧠 TỔNG KẾT

## Bạn đã biết:

* File: đọc / ghi
* Pointer: địa chỉ bộ nhớ
* Struct: dữ liệu đơn giản
* Class: OOP cơ bản

---

# 🚀 NEXT LEVEL

* Vector / Map (STL)
* Con trỏ nâng cao
* File nhị phân
* Project thực tế

```
```
