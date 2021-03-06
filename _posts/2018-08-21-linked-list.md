---
layout: post
title:  "Linked Lists in Python"
author: "Adi Bhamidipati"
---

Linked list is list of nodes connected by pointers. Each node stores data and pointer to next node.
Linkedlist is a dynamic datastucture, so size can be easily increased.

Few frequently used terms in linkedlist are:
1) Node
2) Head
3) Tail
4) Sentinel

Python implementation of the node  is:
class ListNode(self, val):
	def __int__(self, val):
	self.val = val
	self.next = next

The start of the linkedlist is called head, end of the list is tail, whose next pointer points to None.
Sentinel node is a dummy node added at the head or tail of the list to make operations easier on the list.

There are three types of linkedlists
1) Singly linked list, have uni-directional pointers to next immediate node in uni direction
2) Doubly linked list, have bi-directional pointers to neighboring nodes
3) Circular linked list, have uni-directional pointers to the next node and tail points to the head of the list

Applications of LinkedLists are:

1) Linear linkedlists are used to implement stacks. It would be FILO [first in last out] procedure to access data.

2) Doubly Linkedlists  used in implementation of buffer to provide undo/redo feature to word application or photoshop application

3) Circular linkedlists are used to implement round robin technique for process scheduling in operating systems.

4) Program stack trace is also a implementation of linkedlists.

5) Browser back and forward button are implementation of the linkedlist concepts

6) Used in implementation of other datastructures like graphs, trees, stacks and queues

7) LRU cache is implemented using linkedlists

8) Implementation of polynomial addition

Time complexity of queues is:
