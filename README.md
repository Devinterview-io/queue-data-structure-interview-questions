# ⚫ Queues in Tech Interviews 2024: Top 9 Questions & Answers

**Queues** are linear data structures that follow the First In, First Out (FIFO) principle, ensuring that the first element added is the first element to be removed. They are fundamental in various computer operations like task scheduling and breadth-first search. In coding interviews, questions about queues assess a candidate's understanding of **sequential data processing** and its applications in different scenarios.

Check out our carefully selected list of **basic** and **advanced** Queues questions and answers to be well-prepared for your tech interviews in 2024.

![Queues Decorative Image](https://storage.googleapis.com/dev-stack-app.appspot.com/blogImg/queues.png?GoogleAccessId=firebase-adminsdk-bgeaf%40dev-stack-app.iam.gserviceaccount.com&Expires=1698606377&Signature=CbC%2FYlCci65sfckJx6cR%2BwByfX7Byj75nEDAFBjUEfnb0aH9sw0be4K46ZvFzELv%2FCTGUg5lge3f9Z7rll12sXv7jlILGQ9f1jmo6pR9AP4mvAQudZDJbZ7Q%2BlhdKoAVEeLFMilAlP%2FhnITj1%2B5jRImnyC1KuvrTOabogv6hY0rTVBRzV7THc3ZhH9XQijVZo5kwV4d3gVlk5o2vTuUTnokglQtSUrdAJPIFwYHOGI8L4G%2FroZN68hwaibBCVvND%2FFtKOPN70Ms9ny8Kn1u9yBG%2Fw%2FecpjgLIJ4S2meNAQBnwvXWkwcXmjBKfoo5k16IiRSSaGwNPFIjNgTlTxgCsA%3D%3D)

👉🏼 You can also find all answers here: [Devinterview.io - Queues](https://devinterview.io/data/queues-interview-questions)

---

## 🔹 1. What is a _Queue_?

### Answer

A **queue** is a data structure that adheres to the **First-In-First-Out (FIFO)** principle and is designed to hold a collection of elements.

### Core Operations

-  **Enqueue**: Adding an element to the end of the queue.
-  **Dequeue**: Removing an element from the front of the queue.
- **IsEmpty**: Checks if the queue is empty.
- **IsFull**: Checks if the queue has reached its capacity.
- **Peek**: Views the front element without removal.

All operations have a space complexity of $O(1)$ and time complexity of $O(1)$, except for **Search**, which has $O(n)$ time complexity.

### Key Characteristics

1. **Order**: Maintains the order of elements according to their arrival time.
2. **Size**: Can be either bounded (fixed size) or unbounded (dynamic size).
3. **Accessibility**: Typically provides only restricted access to elements in front and at the rear.
4. **Time Complexity**: The time required to perform enqueue and dequeue is usually $O(1)$.

### Visual Representation

![Queue](https://firebasestorage.googleapis.com/v0/b/dev-stack-app.appspot.com/o/queues%2Fsimple-queue.svg?alt=media&token=976157b7-407b-4523-b8df-61f79bc1fafc)

### Real-World Examples

-  **Ticket Counter**: People form a queue, and the first person who joined the queue gets the ticket first.
-  **Printer Queue**: Print jobs are processed in the order they were sent to the printer.

### Practical Applications

1. **Task Scheduling**: Used by operating systems for managing processes ready to execute or awaiting specific events.
2. **Handling of Requests**: Servers in multi-threaded environments queue multiple user requests, processing them in arrival order.
3. **Data Buffering**: Supports asynchronous data transfers between processes, such as in IO buffers and pipes.
4. **Breadth-First Search**: Employed in graph algorithms, like BFS, to manage nodes for exploration.
5. **Order Processing**: E-commerce platforms queue customer orders for processing.
6. **Call Center Systems**: Incoming calls wait in a queue before connecting to the next available representative.

### Code Example: Queue

Here is the Python code:

```python
from collections import deque

class Queue:
    def __init__(self):
        self.queue = deque()

    def enqueue(self, item):
        self.queue.append(item)

    def dequeue(self):
        if not self.is_empty():
            return self.queue.popleft()
        raise Exception("Queue is empty.")

    def size(self):
        return len(self.queue)

    def is_empty(self):
        return len(self.queue) == 0

    def front(self):
        if not self.is_empty():
            return self.queue[0]
        raise Exception("Queue is empty.")

    def rear(self):
        if not self.is_empty():
            return self.queue[-1]
        raise Exception("Queue is empty.")

# Example Usage
q = Queue()
q.enqueue(5)
q.enqueue(6)
q.enqueue(3)
q.enqueue(2)
q.enqueue(7)
print("Queue:", list(q.queue))
print("Front:", q.front())
print("Rear:", q.rear())
q.dequeue()
print("After dequeue:", list(q.queue))
```

---

## 🔹 2. Name some _Types of Queue_.

### Answer

**Queues** are adaptable data structures with diverse types, each optimized for specific tasks. Let's explore the different forms of queues and their functionalities.

### Simple Queue

A **Simple Queue** follows the basic **FIFO** principle. This means items are added at the end and removed from the beginning.

#### Visual Representation

![Simple Queue](https://firebasestorage.googleapis.com/v0/b/dev-stack-app.appspot.com/o/queues%2Fsimple-queue.svg?alt=media&token=976157b7-407b-4523-b8df-61f79bc1fafc)

#### Implementation

Here is the Python code:

```python
class SimpleQueue:
    def __init__(self):
        self.queue = []
    
    def enqueue(self, item):
        self.queue.append(item)
    
    def dequeue(self):
        if not self.is_empty():
            return self.queue.pop(0)
    
    def is_empty(self):
        return len(self.queue) == 0
    
    def size(self):
        return len(self.queue)
```

### Circular Queue

In a **Circular Queue** the last element points to the first element, making a circular link.  This structure uses a **fixed-size array** and can wrap around upon reaching the end. It's more **memory efficient** than a Simple Queue, reusing positions at the front that are left empty by the dequeue operations.

#### Visual Representation

![Circular Queue](https://firebasestorage.googleapis.com/v0/b/dev-stack-app.appspot.com/o/queues%2Fcircular-queue.svg?alt=media&token=31e68b64-92a8-45f7-84c4-0ba8eb929ee8)

#### Implementation

Here is the Python code:

```python
class CircularQueue:
    def __init__(self, k):
        self.queue = [None] * k
        self.size = k
        self.front = self.rear = -1
    
    def enqueue(self, item):
        if self.is_full():
            return "Queue is full"
        elif self.is_empty():
            self.front = self.rear = 0
        else:
            self.rear = (self.rear + 1) % self.size
        self.queue[self.rear] = item
    
    def dequeue(self):
        if self.is_empty():
            return "Queue is empty"
        elif self.front == self.rear:
            temp = self.queue[self.front]
            self.front = self.rear = -1
            return temp
        else:
            temp = self.queue[self.front]
            self.front = (self.front + 1) % self.size
            return temp
    
    def is_empty(self):
        return self.front == -1
    
    def is_full(self):
        return (self.rear + 1) % self.size == self.front
```

### Priority Queue

A **Priority Queue** gives each item a priority. Items with higher priorities are dequeued before those with lower priorities. This is useful in scenarios like task scheduling where some tasks need to be processed before others.

#### Visual Representation

![Priority Queue](https://firebasestorage.googleapis.com/v0/b/dev-stack-app.appspot.com/o/queues%2Fpriority-queue.svg?alt=media&token=df8214e1-9ba6-4aaf-9f79-bd5334a234af)

#### Implementation

Here is the Python code:

```python
class PriorityQueue:
    def __init__(self):
        self.queue = []
    
    def enqueue(self, item, priority):
        self.queue.append((item, priority))
        self.queue.sort(key=lambda x: x[1], reverse=True)
    
    def dequeue(self):
        if not self.is_empty():
            return self.queue.pop(0)[0]
    
    def is_empty(self):
        return len(self.queue) == 0
```

### Double-Ended Queue (De-queue)

A **Double-Ended Queue** allows items to be added or removed from both ends, giving it **more flexibility** compared to a simple queue.

#### Visual Representation

![De-queue](https://firebasestorage.googleapis.com/v0/b/dev-stack-app.appspot.com/o/queues%2Fdouble-ended.svg?alt=media&token=acca0731-3dd3-4af0-bbad-86739fb0506a)

#### Implementation

Here is the Python code:

```python
from collections import deque

de_queue = deque()
de_queue.append(1)  # Add to rear
de_queue.appendleft(2)  # Add to front
de_queue.pop()  # Remove from rear
de_queue.popleft()  # Remove from front
```

### Input-Restricted Deque and Output-Restricted Deque

An **Input-Restricted Deque** only allows items to be added at one end, while an **Output-Restricted Deque** limits removals to one end.

#### Visual Representation

**Input-Restricted Deque**

![Input-Restricted Deque](https://firebasestorage.googleapis.com/v0/b/dev-stack-app.appspot.com/o/queues%2Fimput-restricted-deque.svg?alt=media&token=6ca0c591-ed53-40be-b410-3aea8fa519b0)

**Output-Restricted Deque**

![Output-Restricted Deque](https://firebasestorage.googleapis.com/v0/b/dev-stack-app.appspot.com/o/queues%2Foutput-restricted-deque.svg?alt=media&token=d304afbd-5ac3-47bb-b58e-759648c0761d)

---

## 🔹 3. Name some _Queue Implementations_. Compare their efficiency.

### Answer

**Queues** can be built using various underlying structures, each with its trade-offs in efficiency and complexity.

### Naive Implementations

#### Simple Array

Using a simple array for implementation requires **shifting elements** when adding or removing from the front. This makes operations linear time $O(n)$, which is **inefficient** and not suitable for large queues or real-time use.

```python
class ArrayQueue:
    def __init__(self):
        self.queue = []

    def enqueue(self, item):
        self.queue.append(item)

    def dequeue(self):
        return self.queue.pop(0)
```

#### Singly-linked List

Using a singly-linked list allows $O(1)$ `enqueue` with a tail pointer but still $O(n)$ `dequeue`.

```python
class Node:
    def __init__(self, data=None):
        self.data = data
        self.next = None

class LinkedListQueue:
    def __init__(self):
        self.head = None
        self.tail = None

    def enqueue(self, item):
        new_node = Node(item)
        if self.tail:
            self.tail.next = new_node
        else:
            self.head = new_node
        self.tail = new_node

    def dequeue(self):
        if self.head:
            data = self.head.data
            self.head = self.head.next
            if not self.head:
                self.tail = None
            return data
```

### Efficient Implementations

#### Doubly Linked List

A doubly linked list enables $O(1)$ `enqueue` and `dequeue` by maintaining head and tail pointers, but it requires **prev node management**.

```python
class DNode:
    def __init__(self, data=None):
        self.data = data
        self.next = None
        self.prev = None

class DoublyLinkedListQueue:
    def __init__(self):
        self.head = None
        self.tail = None

    def enqueue(self, item):
        new_node = DNode(item)
        if not self.head:
            self.head = new_node
        else:
            self.tail.next = new_node
            new_node.prev = self.tail
        self.tail = new_node

    def dequeue(self):
        if self.head:
            data = self.head.data
            self.head = self.head.next
            if self.head:
                self.head.prev = None
            else:
                self.tail = None
            return data
```

#### Double-Ended Queue

The `collections.deque` in Python is essentially a double-ended queue implemented using a **doubly-linked list**, providing $O(1)$ complexities for operations at both ends.

```python
from collections import deque

class DequeQueue:
    def __init__(self):
        self.queue = deque()

    def enqueue(self, item):
        self.queue.append(item)

    def dequeue(self):
        return self.queue.popleft()
```

#### Binary Heap

A binary heap with its **binary tree structure** is optimized for **priority queues**, achieving $O(\log n)$ for both `enqueue` and `dequeue` operations. This makes it useful for situations where you need to process elements in a particular order.

```python
import heapq

class MinHeapQueue:
    def __init__(self):
        self.heap = []

    def enqueue(self, item):
        heapq.heappush(self.heap, item)

    def dequeue(self):
        return heapq.heappop(self.heap)
```

---

## 🔹 4. How to manage _Full Circular Queue Event_?

### Answer

When a **Circular Queue** is full, you have to make a decision on how to handle new incoming items. This is known as the **Full Circular Queue Event**.

There are several strategies to manage this event:

### 1. Discard New Item

The simplest approach is to **discard** any new incoming item when the queue is full. Neither the **head** nor the **tail** pointers are updated.

#### Example: Server Request Handling

One real-life example where this strategy is employed is in server request handling. If a server is already at full capacity and unable to accommodate new incoming requests, it may choose to simply drop those requests.

#### Code Example: Discarding Requests

Here is the Python code:

```python
def enqueue(self, item):
    if self.is_full():
        print("Queue is full. Discarding new item.")
    else:
        # Normal enqueue operation
        self.tail = (self.tail + 1) % self.size
        self.queue[self.tail] = item
```

### 2. Discard Oldest Item

Another strategy is to discard the oldest item in the queue to make room for the new one. Both the **head** and the **tail** pointers are moved one step forward.

#### Example: Real-time Video Streaming

In real-time video applications, you might want to prioritize the latest frames. So, if the buffer is full, the oldest frame in the buffer can be discarded.

#### Code Example: Buffering Live Video

Here is the Python code:

```python
def enqueue(self, item):
    if self.is_full():
        self.head = (self.head + 1) % self.size  # Move head pointer forward
        self.tail = (self.tail + 1) % self.size  # Move tail pointer forward
        self.queue[self.tail] = item
    else:
        # Normal enqueue operation
        self.tail = (self.tail + 1) % self.size
        self.queue[self.tail] = item
```

### 3. Increase Queue Size Dynamically

You can also opt to increase the size of the queue dynamically to accommodate new items. This involves reallocating more memory for the underlying buffer.

#### Example: Dynamic Memory Allocation

For certain applications where it is crucial to not lose any data, dynamically increasing the queue size can be a useful strategy.

#### Code Example: Dynamically Increasing The Queue Size

```python
def enqueue(self, item):
    if self.is_full():
        self.size *= 2  # Double the size of the queue
        new_queue = [None] * self.size
        for i, val in enumerate(self.queue):
            new_queue[i] = val
        self.queue = new_queue
        self.tail = (self.tail + 1) % self.size
        self.queue[self.tail] = item
    else:
        # Normal enqueue operation
        self.tail = (self.tail + 1) % self.size
        self.queue[self.tail] = item
```

---
## 🔹 5. When should I use _Stack_ or _Queue_ data structures instead of _Arrays/Lists_?

### Answer

👉🏼 Check out all 9 answers here: [Devinterview.io - Queues](https://devinterview.io/data/queues-interview-questions)

---

## 🔹 6. Name the _Most Efficient_ way to implement _Stack_ and _Queue_ together.

### Answer

👉🏼 Check out all 9 answers here: [Devinterview.io - Queues](https://devinterview.io/data/queues-interview-questions)

---

## 🔹 7. Implement a _Queue_ using _Two Stacks_.

### Answer

👉🏼 Check out all 9 answers here: [Devinterview.io - Queues](https://devinterview.io/data/queues-interview-questions)

---

## 🔹 8. Implement a _Queue_ using only _One Stack_.

### Answer

👉🏼 Check out all 9 answers here: [Devinterview.io - Queues](https://devinterview.io/data/queues-interview-questions)

---

## 🔹 9. Implement _Stack_ using _Two Queues_ with efficient push.

### Answer

👉🏼 Check out all 9 answers here: [Devinterview.io - Queues](https://devinterview.io/data/queues-interview-questions)

---

