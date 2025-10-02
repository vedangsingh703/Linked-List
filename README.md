# Linked-List
# LINKED LIST IN CPP

Aim: To study and implement Linked Lists in Cpp.

Tools Used: VS Code or Programiz online compiler.

# Theory

# Linked Lists in Cpp
A linked list in C++ is a linear data structure where elements, called nodes, are connected through pointers. Each node usually contains two parts: the data and a pointer to the next node. Unlike arrays, linked lists are not stored in contiguous memory locations, which makes them more flexible as their size can grow or shrink dynamically at runtime. There are different types of linked lists such as singly, doubly, and circular. In a singly linked list, nodes point only to the next node, while in a doubly linked list, each node has pointers to both the next and previous nodes. A circular linked list connects the last node back to the first node, forming a loop. Linked lists are efficient for insertion and deletion operations at known positions, typically requiring constant time. However, random access is slower compared to arrays, as it requires traversal of nodes one by one. Thus, linked lists are useful when dynamic memory management and frequent insertions or deletions are required.

```

#include <iostream>
using namespace std;

// Node structure
struct Node {
    int data;
    Node* next;
};

// Linked List class
class LinkedList {
private:
    Node* head;

public:
    // Constructor
    LinkedList() { head = nullptr; }

    // Insert at beginning
    void insertAtBeginning(int value);

    // Insert at end
    void insertAtEnd(int value);

    // Delete a node
    void deleteNode(int value);

    // Display list
    void display();

    // Destructor
    ~LinkedList();
};

```

**--> Types of Linked Lists:-**

1. Singly Linked List – Each node has data and a pointer to the next node. Traversal is only in one direction.
2. Doubly Linked List – Each node has data, a pointer to the next node, and a pointer to the previous node. Traversal is possible in both directions.
3. Circular Singly Linked List – Similar to a singly linked list, but the last node points back to the first node, forming a circle.
4. Circular Doubly Linked List – Similar to a doubly linked list, but the last node’s next pointer connects to the first node, and the first node’s previous pointer connects to the last node.

Here, we have worked on singly linked lists.

# Program-1: Implementation of Node Structure in Singly Linked List
A linked list is a dynamic data structure consisting of nodes connected through pointers. Each node typically stores data and the address of the next node. In this program, a simple Node class is created with an integer value and a pointer to the next node. A new node is allocated dynamically using the constructor, which initializes the data and sets the next pointer to NULL. This forms the basic building block of a singly linked list, which can later be extended to create chains of nodes.

--> Algorithm:

1. Start
2. Define a Node class with:
  --An integer variable val to store data.
  --A pointer next to point to the next node.
3. Create a constructor to initialize val with given data and set next = NULL.
4. In the main() function:
  --Dynamically create a new node using the Node constructor.
  --Store a value (e.g., 20) in the node.
  --Print the node’s data and its next pointer.
6. End

# Program-2: Creation and Traversal of Singly Linked List
A singly linked list is a linear data structure where each node contains data and a pointer to the next node. In this program, three nodes are dynamically created and linked together to form a list. The next pointer of each node connects it to the following node, while the last node points to NULL. Traversal is performed using a temporary pointer that iterates through the list until the end. This demonstrates the basic concept of creating and displaying a singly linked list in C++.

--> Algorithm:

1. Start
2. Define a Node class with:
  --Integer val for data.
  --Pointer next for linking nodes.
3. Create a constructor to initialize val with given data and set next = NULL.
4. In main() function:
  --Dynamically create three nodes n1, n2, n3 with values 10, 20, 30.
  --Link nodes: n1->next = n2, n2->next = n3.
5. Initialize a temporary pointer temp = n1.
6. Repeat until temp == NULL:
  --Print temp->val.
  --Move temp = temp->next.
7. End traversal when the last node is reached (temp = NULL).
8. Stop

# Program-3: Insertion at Head in Singly Linked List
In a singly linked list, insertion at the head means adding a new node at the beginning of the list. Each new node is created dynamically and its next pointer is set to the current head. Then the head pointer is updated to this new node, making it the first element. This method is efficient as it takes constant time, O(1), for insertion. The program also includes a display function to traverse the list and print all node values until NULL is reached. Thus, it demonstrates dynamic insertion and traversal of a singly linked list.

--> Algorithm:

1. Start
2. Define a Link class with:
  --Integer data for storing value.
  --Pointer next to point to the next node.
3. Create a constructor to initialize data with the given value and next = NULL.
4. To insert a node at the head:
  --Create a new node dynamically with the given data.
  --Set new_node->next = head.
  --Update head = new_node.
5. To display the list:
  --Initialize a temporary pointer temp = head.
  --While temp != NULL, print temp->data and move temp = temp->next.
6. Repeat insertion steps for each new element.
7. Stop

# Conclusion
These three programs together demonstrate the fundamental concepts of singly linked lists in C++. Program-1 shows the creation of a single node, highlighting the structure of a node with data and a pointer to the next element. Program-2 extends this by linking multiple nodes to form a list and traversing it to access each element sequentially. Program-3 illustrates insertion at the head, where new nodes are dynamically added at the beginning and the head pointer is updated accordingly. Collectively, these programs provide a clear understanding of node creation, list formation, traversal, and dynamic insertion, which are essential operations in singly linked lists.
