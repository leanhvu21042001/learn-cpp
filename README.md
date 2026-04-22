# 🚀 C++ Cơ Bản – Cheat Sheet Full

---

## 🧱 1. Cấu trúc chương trình

```cpp
#include <iostream>
using namespace std;

int main() {
    return 0;
}
```

---

## 🧠 2. Biến & Kiểu dữ liệu

### Khai báo

```cpp
int a = 10;
float b = 3.14;
double c = 3.14159;
char d = 'A';
string e = "Hello";
bool f = true;
```

### Hằng số

```cpp
const int MAX = 100;
```

### Ép kiểu

```cpp
double b = (double)a;
```

---

## ⌨️ 3. Nhập / Xuất (CMD)

### Xuất

```cpp
cout << "Hello" << endl;
```

### Nhập

```cpp
int a;
cin >> a;
```

### Nhập nhiều biến

```cpp
int a, b;
cin >> a >> b;
```

### Nhập chuỗi có khoảng trắng

```cpp
string s;
getline(cin, s);
```

### Fix lỗi getline sau cin

```cpp
cin.ignore();
getline(cin, s);
```

---

## ⚡ 4. Toán tử

### Toán học

```
+  -  *  /  %
```

### So sánh

```
==  !=  >  <  >=  <=
```

### Logic

```
&&   ||   !
```

---

## 🔀 5. Điều kiện

### if

```cpp
if (a > 10) {
    cout << "Lon hon 10";
}
```

### if-else

```cpp
if (a > 10) {
    cout << "Lon";
} else {
    cout << "Nho";
}
```

### if-else if

```cpp
if (a > 10) {
    cout << "Lon";
} else if (a == 10) {
    cout << "Bang";
} else {
    cout << "Nho";
}
```

### switch

```cpp
switch (x) {
    case 1:
        cout << "One";
        break;
    case 2:
        cout << "Two";
        break;
    default:
        cout << "Other";
}
```

---

## 🔁 6. Vòng lặp

### for

```cpp
for (int i = 0; i < 5; i++) {
    cout << i;
}
```

### while

```cpp
int i = 0;
while (i < 5) {
    cout << i;
    i++;
}
```

### do-while

```cpp
int i = 0;
do {
    cout << i;
    i++;
} while (i < 5);
```

### break / continue

```cpp
if (i == 5) break;
if (i % 2 == 0) continue;
```

---

## 🧩 7. Hàm (Function)

### Hàm trả về

```cpp
int sum(int a, int b) {
    return a + b;
}
```

### Gọi hàm

```cpp
int result = sum(3, 5);
```

### Hàm void

```cpp
void hello() {
    cout << "Hello";
}
```

### Tham chiếu

```cpp
void update(int &a) {
    a = 100;
}
```

### Tham số mặc định

```cpp
int sum(int a, int b = 10) {
    return a + b;
}
```

---

## 📦 8. Mảng (Array)

```cpp
int arr[5] = {1,2,3,4,5};
```

```cpp
for (int i = 0; i < 5; i++) {
    cout << arr[i];
}
```

---

## 🔤 9. String

```cpp
string s = "hello";
cout << s.length();
```

---

## ⚡ 10. Input nâng cao

### Nhập nhiều dòng

```cpp
string s;
while (getline(cin, s)) {
    cout << s;
}
```

### Đọc đến EOF

```cpp
int x;
while (cin >> x) {
    cout << x;
}
```

---

## 🎯 11. Demo tổng hợp

```cpp
#include <iostream>
using namespace std;

int sum(int a, int b) {
    return a + b;
}

int main() {
    int a, b;
    cin >> a >> b;

    if (a > b) {
        cout << "a lon hon b\n";
    } else {
        cout << "a <= b\n";
    }

    for (int i = 0; i < a; i++) {
        cout << i << " ";
    }

    cout << "\nTong = " << sum(a, b);
}
```

---

## 🧠 Tổng kết

Cần nắm:

* cin / cout
* if / switch
* for / while
* function
* array / string

👉 Đủ để code bài cơ bản + CLI app

---

## 🚀 Next Level

* Pointer
* Vector / Map (STL)
* Memory
* Debug C++

```
```
