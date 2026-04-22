# 🧪 C++ Bài Tập Cơ Bản + Đáp Án

---

## 🟢 Bài 1: Tổng 2 số

### Đề bài

Nhập 2 số nguyên, in ra tổng.

### Code mẫu

```cpp
#include <iostream>
using namespace std;

int main() {
    int a, b;
    cin >> a >> b;
    cout << a + b;
}
```

---

## 🟢 Bài 2: Kiểm tra số chẵn lẻ

### Đề bài

Nhập số nguyên n, kiểm tra chẵn hay lẻ.

### Đáp án

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    cin >> n;

    if (n % 2 == 0) {
        cout << "Chan";
    } else {
        cout << "Le";
    }
}
```

---

## 🟢 Bài 3: Tìm số lớn nhất

### Đề bài

Nhập 3 số, in số lớn nhất.

### Đáp án

```cpp
#include <iostream>
using namespace std;

int main() {
    int a, b, c;
    cin >> a >> b >> c;

    int maxVal = a;
    if (b > maxVal) maxVal = b;
    if (c > maxVal) maxVal = c;

    cout << maxVal;
}
```

---

## 🟡 Bài 4: Tính tổng từ 1 đến n

### Đề bài

Nhập n, tính tổng 1 + 2 + ... + n

### Đáp án

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    cin >> n;

    int sum = 0;
    for (int i = 1; i <= n; i++) {
        sum += i;
    }

    cout << sum;
}
```

---

## 🟡 Bài 5: Tính giai thừa

### Đề bài

Nhập n, tính n!

### Đáp án

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    cin >> n;

    long long fact = 1;
    for (int i = 1; i <= n; i++) {
        fact *= i;
    }

    cout << fact;
}
```

---

## 🟡 Bài 6: Đếm số chữ số

### Đề bài

Nhập số nguyên n, đếm số chữ số.

### Đáp án

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    cin >> n;

    int count = 0;
    if (n == 0) count = 1;

    while (n != 0) {
        n /= 10;
        count++;
    }

    cout << count;
}
```

---

## 🟡 Bài 7: Đảo ngược số

### Đề bài

Nhập số nguyên n, đảo ngược.

### Đáp án

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    cin >> n;

    int rev = 0;
    while (n != 0) {
        rev = rev * 10 + n % 10;
        n /= 10;
    }

    cout << rev;
}
```

---

## 🔵 Bài 8: Kiểm tra số nguyên tố

### Đề bài

Nhập n, kiểm tra có phải số nguyên tố không.

### Đáp án

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    cin >> n;

    if (n < 2) {
        cout << "Khong";
        return 0;
    }

    for (int i = 2; i * i <= n; i++) {
        if (n % i == 0) {
            cout << "Khong";
            return 0;
        }
    }

    cout << "Co";
}
```

---

## 🔵 Bài 9: Mảng - Tìm max

### Đề bài

Nhập n phần tử, tìm max.

### Đáp án

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    cin >> n;

    int arr[1000];
    for (int i = 0; i < n; i++) {
        cin >> arr[i];
    }

    int maxVal = arr[0];
    for (int i = 1; i < n; i++) {
        if (arr[i] > maxVal) {
            maxVal = arr[i];
        }
    }

    cout << maxVal;
}
```

---

## 🔵 Bài 10: Đếm số chẵn trong mảng

### Đề bài

Nhập mảng, đếm số chẵn.

### Đáp án

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    cin >> n;

    int arr[1000];
    for (int i = 0; i < n; i++) {
        cin >> arr[i];
    }

    int count = 0;
    for (int i = 0; i < n; i++) {
        if (arr[i] % 2 == 0) count++;
    }

    cout << count;
}
```

---

## 🔴 Bài 11: Chuỗi - Đếm ký tự

### Đề bài

Nhập chuỗi, đếm số ký tự (không tính khoảng trắng).

### Đáp án

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string s;
    getline(cin, s);

    int count = 0;
    for (char c : s) {
        if (c != ' ') count++;
    }

    cout << count;
}
```

---

## 🔴 Bài 12: Palindrome

### Đề bài

Kiểm tra chuỗi có đối xứng không.

### Đáp án

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string s;
    cin >> s;

    int l = 0, r = s.length() - 1;
    while (l < r) {
        if (s[l] != s[r]) {
            cout << "Khong";
            return 0;
        }
        l++;
        r--;
    }

    cout << "Co";
}
```

---

## 🧠 Gợi ý luyện tập

* Làm lại không nhìn code
* Sửa code sai → hiểu lỗi
* Viết lại bằng cách khác

---

## 🚀 Next Level

* Pointer
* Vector / Map
* Sorting / Searching
* LeetCode Easy → Medium

```
```
