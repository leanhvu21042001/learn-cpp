# 🔗 C++ Node & Linked List – Full Kiến Thức + Bài Tập

---

# 🧠 1. NODE LÀ GÌ?

Node = 1 phần tử trong linked list

Gồm:

* data (giá trị)
* pointer (trỏ tới node tiếp theo)

---

## 🔹 Khai báo Node

```cpp
struct Node {
    int data;
    Node* next;
};
```

---

## 🔹 Tạo node

```cpp
Node* createNode(int value) {
    Node* newNode = new Node;
    newNode->data = value;
    newNode->next = NULL;
    return newNode;
}
```

---

# 🔗 2. SINGLY LINKED LIST

---

## 🔹 Khai báo head

```cpp
Node* head = NULL;
```

---

## 🔹 Thêm vào đầu (push front)

```cpp
void pushFront(Node*& head, int value) {
    Node* newNode = createNode(value);
    newNode->next = head;
    head = newNode;
}
```

---

## 🔹 Thêm vào cuối (push back)

```cpp
void pushBack(Node*& head, int value) {
    Node* newNode = createNode(value);

    if (head == NULL) {
        head = newNode;
        return;
    }

    Node* temp = head;
    while (temp->next != NULL) {
        temp = temp->next;
    }

    temp->next = newNode;
}
```

---

## 🔹 Duyệt danh sách

```cpp
void printList(Node* head) {
    Node* temp = head;

    while (temp != NULL) {
        cout << temp->data << " ";
        temp = temp->next;
    }
}
```

---

## 🔹 Xóa node đầu

```cpp
void popFront(Node*& head) {
    if (head == NULL) return;

    Node* temp = head;
    head = head->next;
    delete temp;
}
```

---

## 🔹 Xóa node cuối

```cpp
void popBack(Node*& head) {
    if (head == NULL) return;

    if (head->next == NULL) {
        delete head;
        head = NULL;
        return;
    }

    Node* temp = head;
    while (temp->next->next != NULL) {
        temp = temp->next;
    }

    delete temp->next;
    temp->next = NULL;
}
```

---

# 🧪 BÀI TẬP LINKED LIST

---

## 🟢 Bài 1: Tạo danh sách & in

```cpp
#include <iostream>
using namespace std;

struct Node {
    int data;
    Node* next;
};

Node* createNode(int value) {
    Node* n = new Node;
    n->data = value;
    n->next = NULL;
    return n;
}

void pushBack(Node*& head, int value) {
    Node* n = createNode(value);

    if (!head) {
        head = n;
        return;
    }

    Node* temp = head;
    while (temp->next) temp = temp->next;

    temp->next = n;
}

void printList(Node* head) {
    while (head) {
        cout << head->data << " ";
        head = head->next;
    }
}

int main() {
    Node* head = NULL;

    pushBack(head, 1);
    pushBack(head, 2);
    pushBack(head, 3);

    printList(head);
}
```

---

## 🟡 Bài 2: Tìm phần tử

```cpp
bool search(Node* head, int x) {
    while (head) {
        if (head->data == x) return true;
        head = head->next;
    }
    return false;
}
```

---

## 🔵 Bài 3: Đếm số node

```cpp
int count(Node* head) {
    int cnt = 0;
    while (head) {
        cnt++;
        head = head->next;
    }
    return cnt;
}
```

---

## 🔴 Bài 4: Đảo ngược linked list

```cpp
Node* reverseList(Node* head) {
    Node* prev = NULL;
    Node* curr = head;

    while (curr) {
        Node* next = curr->next;
        curr->next = prev;

        prev = curr;
        curr = next;
    }

    return prev;
}
```

---

# 🔁 3. DOUBLY LINKED LIST

---

## 🔹 Node 2 chiều

```cpp
struct Node {
    int data;
    Node* prev;
    Node* next;
};
```

---

## 🔹 Thêm đầu

```cpp
void pushFront(Node*& head, int value) {
    Node* n = new Node{value, NULL, head};

    if (head != NULL) {
        head->prev = n;
    }

    head = n;
}
```

---

# 🔄 4. CIRCULAR LINKED LIST

---

## 🔹 Đặc điểm

* Node cuối trỏ về head

```cpp
temp->next = head;
```

---

# 🧠 TỔNG KẾT

## Singly Linked List

* Dễ implement
* Chỉ đi 1 chiều

## Doubly Linked List

* Đi 2 chiều
* Tốn bộ nhớ hơn

## Circular

* Không có NULL
* Loop liên tục

---

# ⚠️ LỖI THƯỜNG GẶP

* Quên `delete` → memory leak
* Trỏ sai → crash
* Không check NULL

---

# 🚀 NEXT LEVEL

* Stack / Queue bằng linked list
* STL list
* Cycle detection (Floyd)
* Merge 2 linked list

```
```
