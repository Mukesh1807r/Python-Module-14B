# Simple Implementation of Priority Queue using Queue

## 📌 Aim
To write a Python program that implements a **Priority Queue** using a regular queue. The priority queue will be implemented with functions for inserting and deleting elements. The elements are arranged in descending order of priority, where the maximum element will always have the highest priority.

---

## 🛠 Procedure
1. Define a class `PriorityQueue` to represent the queue.
   - The queue will be implemented using a list.
   - Define the `insert` function to append an element to the queue.
   - Define the `delete` function to remove the element with the highest priority (maximum value) from the queue.
2. The `insert` function adds an element to the queue, while the `delete` function removes and returns the highest priority element.
3. The `__str__` method allows us to print the current elements in the queue.

---

## 💻 Program

```python
class PriorityQueue(object):
    def __init__(self):
        self.queue = []

    def __str__(self):
        return ' '.join([str(i) for i in self.queue])

    def isEmpty(self):
        return len(self.queue) == 0

    def insert(self, data):
        self.queue.append(data)

    def delete(self):
        if self.isEmpty():
            return "Queue is empty"
        
        max_value = max(self.queue)  
        self.queue.remove(max_value)
        return max_value  

myQueue = PriorityQueue()
n = int(input())  

for i in range(n):
    ele = int(input())
    myQueue.insert(ele)

print(myQueue) 

while not myQueue.isEmpty():
    print(myQueue.delete())
```
---

## Output

![image](https://github.com/user-attachments/assets/b1f08003-6fd1-4c05-8613-a4ef873967eb)

---

## Result 

Thus, the program was successfully created and executed to implement the Priority Queue with the desired insert and delete operations.

