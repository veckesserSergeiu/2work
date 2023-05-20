public class LinkedList {
Node head;

public LinkedList() {
this.head = null;
}

public void add(int data) {
Node newNode = new Node(data);
if (head == null) {
head = newNode;
return;
}
Node current = head;
while (current.next != null) {
current = current.next;
}
current.next = newNode;
}

public void insert(int data, int position) {
Node newNode = new Node(data);
if (position == 0) {
newNode.next = head;
head = newNode;
return;
}
Node current = head;
for (int i = 0; i < position - 1; i++) {
current = current.next;
if (current == null) {
throw new IndexOutOfBoundsException();
}
}
newNode.next = current.next;
current.next = newNode;
}

public void delete(int data) {
if (head == null) {
return;
}
if (head.data == data) {
head = head.next;
return;
}
Node current = head;
while (current.next != null) {
if (current.next.data == data) {
current.next = current.next.next;
return;
}
current = current.next;
}
}
}

Время ответа: 13.04.2023 | 15:26
Попытка #2
Ответ: 
public class Node {
int data;
Node next;

public Node(int data) {
this.data = data;
this.next = null;
}
}
