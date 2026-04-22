# 🚀 C++ Thuật Toán Cơ Bản – Tìm Kiếm & Sắp Xếp

---

# 🔍 1. TÌM KIẾM (SEARCH)

---

## 🟢 Linear Search (Tìm kiếm tuyến tính)

### Ý tưởng

Duyệt từng phần tử

### Code

```cpp id="c1k9n2"
int linearSearch(int arr[], int n, int x) {
    for (int i = 0; i < n; i++) {
        if (arr[i] == x) return i;
    }
    return -1;
}
```

### Độ phức tạp

* O(n)

---

## 🔵 Binary Search (Tìm kiếm nhị phân)

### Điều kiện

* Mảng phải **đã sắp xếp**

### Code

```cpp id="6lb3u5"
int binarySearch(int arr[], int n, int x) {
    int l = 0, r = n - 1;

    while (l <= r) {
        int mid = (l + r) / 2;

        if (arr[mid] == x) return mid;
        else if (arr[mid] < x) l = mid + 1;
        else r = mid - 1;
    }

    return -1;
}
```

### Độ phức tạp

* O(log n)

---

# 🧪 BÀI TẬP SEARCH

---

## 🟢 Bài 1: Linear Search

Nhập mảng, tìm x

```cpp id="3fpk7o"
#include <iostream>
using namespace std;

int main() {
    int n, x;
    cin >> n;

    int arr[1000];
    for (int i = 0; i < n; i++) cin >> arr[i];

    cin >> x;

    for (int i = 0; i < n; i++) {
        if (arr[i] == x) {
            cout << i;
            return 0;
        }
    }

    cout << -1;
}
```

---

## 🔵 Bài 2: Binary Search

```cpp id="o8mqxq"
#include <iostream>
using namespace std;

int main() {
    int n, x;
    cin >> n;

    int arr[1000];
    for (int i = 0; i < n; i++) cin >> arr[i];

    cin >> x;

    int l = 0, r = n - 1;

    while (l <= r) {
        int mid = (l + r) / 2;

        if (arr[mid] == x) {
            cout << mid;
            return 0;
        } else if (arr[mid] < x) {
            l = mid + 1;
        } else {
            r = mid - 1;
        }
    }

    cout << -1;
}
```

---

# 🔃 2. SẮP XẾP (SORT)

---

## 🟢 Bubble Sort

### Ý tưởng

So sánh từng cặp

```cpp id="8h7mzm"
void bubbleSort(int arr[], int n) {
    for (int i = 0; i < n - 1; i++) {
        for (int j = 0; j < n - i - 1; j++) {
            if (arr[j] > arr[j + 1]) {
                swap(arr[j], arr[j + 1]);
            }
        }
    }
}
```

### Độ phức tạp

* O(n²)

---

## 🟡 Selection Sort

```cpp id="2g6e2p"
void selectionSort(int arr[], int n) {
    for (int i = 0; i < n - 1; i++) {
        int minIdx = i;

        for (int j = i + 1; j < n; j++) {
            if (arr[j] < arr[minIdx]) {
                minIdx = j;
            }
        }

        swap(arr[i], arr[minIdx]);
    }
}
```

---

## 🔵 Insertion Sort

```cpp id="s3dx5b"
void insertionSort(int arr[], int n) {
    for (int i = 1; i < n; i++) {
        int key = arr[i];
        int j = i - 1;

        while (j >= 0 && arr[j] > key) {
            arr[j + 1] = arr[j];
            j--;
        }

        arr[j + 1] = key;
    }
}
```

---

## 🔥 Quick Sort (quan trọng)

```cpp id="m9a0l6"
int partition(int arr[], int low, int high) {
    int pivot = arr[high];
    int i = low - 1;

    for (int j = low; j < high; j++) {
        if (arr[j] < pivot) {
            i++;
            swap(arr[i], arr[j]);
        }
    }

    swap(arr[i + 1], arr[high]);
    return i + 1;
}

void quickSort(int arr[], int low, int high) {
    if (low < high) {
        int pi = partition(arr, low, high);

        quickSort(arr, low, pi - 1);
        quickSort(arr, pi + 1, high);
    }
}
```

### Độ phức tạp

* Trung bình: O(n log n)

---

# 🧪 BÀI TẬP SORT

---

## 🟢 Bài 3: Bubble Sort

```cpp id="pqzv0t"
#include <iostream>
using namespace std;

int main() {
    int n;
    cin >> n;

    int arr[1000];
    for (int i = 0; i < n; i++) cin >> arr[i];

    for (int i = 0; i < n - 1; i++) {
        for (int j = 0; j < n - i - 1; j++) {
            if (arr[j] > arr[j + 1]) {
                swap(arr[j], arr[j + 1]);
            }
        }
    }

    for (int i = 0; i < n; i++) cout << arr[i] << " ";
}
```

---

## 🔵 Bài 4: Quick Sort

```cpp id="aqc1jh"
#include <iostream>
using namespace std;

int partition(int arr[], int low, int high) {
    int pivot = arr[high];
    int i = low - 1;

    for (int j = low; j < high; j++) {
        if (arr[j] < pivot) {
            i++;
            swap(arr[i], arr[j]);
        }
    }

    swap(arr[i + 1], arr[high]);
    return i + 1;
}

void quickSort(int arr[], int low, int high) {
    if (low < high) {
        int pi = partition(arr, low, high);

        quickSort(arr, low, pi - 1);
        quickSort(arr, pi + 1, high);
    }
}

int main() {
    int n;
    cin >> n;

    int arr[1000];
    for (int i = 0; i < n; i++) cin >> arr[i];

    quickSort(arr, 0, n - 1);

    for (int i = 0; i < n; i++) cout << arr[i] << " ";
}
```

---

# 🧠 TỔNG KẾT

## SEARCH

* Linear: dễ, chậm
* Binary: nhanh, cần sort

## SORT

* Bubble / Selection: dễ
* Insertion: tốt cho mảng nhỏ
* Quick Sort: mạnh nhất

---

# 🚀 NEXT LEVEL

* Merge Sort
* Heap Sort
* STL sort()
* Two pointers
* Sliding window

```
```
