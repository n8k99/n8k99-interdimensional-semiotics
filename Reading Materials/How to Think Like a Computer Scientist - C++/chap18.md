---
title: "Chapter 18: Linked lists"
type: "[[Reading]]"
domain: "[[The Commons]]"
Lifestage: "🌱 Seed"
status: recovered
source: eckenrodehouse.net (Wayback)
created: "[[2026-06-09]]"
updated: "[[2026-06-09]]"
partOf: "[[How to Think Like a Computer Scientist - C++]]"
tags: [reading, recovered, eckenrodehouse, programming]
---

# Chapter 18: Linked lists

> Recovered from eckenrodehouse.net via the Wayback Machine. Part of [[How to Think Like a Computer Scientist - C++]].

---

# Linked lists

  

### 18.1 References in objects

One of the more interesting qualities of an object is that an object can contain a reference to another object of the same type. There is a common data structure, the **list**, that takes advantage of this feature.

Lists are made up of **nodes**, where each node contains a pointer or reference to the next node in the list. In addition, each node usually contains a unit of data called the **cargo**. In our first example, the cargo will be a single integer, but later we will write a **generic** list that can contain objects of any type.

  

### 18.2 Revenge of the Node

As usual when we write a new class, we'll start with the instance variables, one or two constructors and toString so that we can test the basic mechanism of creating and displaying the new type.

struct Node {
  
  
    public:
  
  
      int cargo;
  
      Node\* next;
  
  
      Node () {
  
          cargo = 0;

  
      }
  
  
      Node (int Cargo, Node Next) {
  
            cargo = Cargo;

  
      }
  
  
      pstring toString () {
  
        pstring s;
  
        for(; n; n/=10)
  
        s = char(n%10 + '0') + s;
  
        return s;
  
      }
  
}
  

The declarations of the instance variables follow naturally from the specification, and the rest follows mechanically from the instance variables. The expression cargo + "" is an awkward but concise way to convert an integer to a String.

To test the implementation so far, we would put something like this in main:

    Node node = new Node (1, null);
  
    cout << node.cargo;
  

The result is simply

1
  

To make it interesting, we need a list with more than one node!

    Node node1 = new Node (1, null);
  
    Node node2 = new Node (2, null);
  
    Node node3 = new Node (3, null);
  

This code creates three nodes, but we don't have a list yet because the nodes are not **linked**. The state diagram looks like this:

![](images/list1.png)

To link up the nodes, we have to make the first node refer to the second and the second node refer to the third.

    node1.next = node2;
  
    node2.next = node3;
  
    node3.next = null;
  

The reference of the third node is null, which indicates that it is the end of the list. Now the state diagram looks like:

![](images/list2.png)

Now we know how to create nodes and link them into lists. What might be less clear at this point is why. Now that we're a little more familiar with the use of the struct Node, we can now introduce you to the other style of notation. The use of dot notation can be replaced by the more well-known ->

For example:

    node1->next = node2;
  
    node2->next = node3;
  
    node3->next = null;
  
  

### 18.3 Lists as collections

The thing that makes lists useful is that they are a way of assembling multiple objects into a single entity, sometimes called a collection. In the example, the first node of the list serves as a reference to the entire list.

If we want to pass the list as a parameter, all we have to pass is a reference to the first node. For example, the method printList takes a single node as an argument. Starting with the head of the list, it prints each node until it gets to the end (indicated by the null reference).

    void printList (Node \*list) {
  
        Node \*node = list;
  
  
        while (node != null) {
  
            cout << node->cargo; << endl;
  
            node = node->next;
  
        }
  
    }
  

To invoke this method we just have to pass a reference to the first node:

        printList (node1);
  

Inside printList we have a reference to the first node of the list, but there is no variable that refers to the other nodes. We have to use the next value from each node to get to the next node.

This diagram shows the value of list and the values that node takes on:

![](images/list3.png)

This way of moving through a list is called a **traversal**, just like the similar pattern of moving through the elements of an array. It is common to use a loop variable like node to refer to each of the nodes in the list in succession.

The output of this method is

123
  

By convention, lists are printed in parentheses with commas between the elements, as in (1, 2, 3). As an exercise, modify printList so that it generates output in this format.

As another exercise, rewrite printList using a for loop instead of a while loop.

  

### 18.4 Lists and recursion

Recursion and lists go together like fava beans and a nice Chianti. For example, here is a recursive algorithm for printing a list backwards:

1. Separate the list into two pieces: the first node (called the head) and the rest (called the tail).
2. Print the tail backwards.
3. Print the head.

Of course, Step 2, the recursive call, assumes that we have a way of printing a list backwards. But *if* we assume that the recursive call works---the leap of faith---then we can convince ourselves that this algorithm works.

All we need is a base case, and a way of proving that for any list we will eventually get to the base case. A natural choice for the base case is a list with a single element, but an even better choice is the empty list, represented by null.

    printBackward (Node \*list) {
  
        if (list == null) return;
  
  
        Node \*head = list;
  
        Node \*tail = list->next;
  
  
        printBackward (tail);
  
        cout << head->cargo;
  
    }
  

The first line handles the base case by doing nothing. The next two lines split the list into head and tail. The last two lines print the list.

We invoke this method exactly as we invoked printList:

        printBackward (node1);
  

The result is a backwards list.

Can we prove that this method will always terminate? In other words, will it always reach the base case? In fact, the answer is no. There are some lists that will make this method crash.

  

### 18.5 Infinite lists

There is nothing to prevent a node from referring back to an earlier node in the list, including itself. For example, this figure shows a list with two nodes, one of which refers to itself.

![](images/list4.png)

If we invoke printList on this list, it will loop forever. If we invoke printBackward it will recurse infinitely. This sort of behavior makes infinite lists difficult to work with.

Nevertheless, they are occasionally useful. For example, we might represent a number as a list of digits and use an infinite list to represent a repeating fraction.

Regardless, it is problematic that we cannot prove that printList and printBackward terminate. The best we can do is the hypothetical statement, "If the list contains no loops, then these methods will terminate." This sort of claim is called a **precondition**. It imposes a constraint on one of the parameters and describes the behavior of the method if the constraint is satisfied. We will see more examples soon.

  

### 18.6 The fundamental ambiguity theorem

There is a part of printBackward that might have raised an eyebrow:

        Node \*head = list;
  
        Node \*tail = list->next;
  

After the first assignment, head and list have the same type and the same value. So why did I create a new variable?

The reason is that the two variables play different roles. We think of head as a reference to a single node, and we think of list as a reference to the first node of a list. These "roles" are not part of the program; they are in the mind of the programmer.

The second assignment creates a new reference to the second node in the list, but in this case we think of it as a list. So, even though head and tail have the same type, they play different roles.

This ambiguity is useful, but it can make programs with lists difficult to read. I often use variable names like node and list to document how I intend to use a variable, and sometimes I create additional variables to disambiguate.

I could have written printBackward without head and tail, but I think it makes it harder to understand:

    void printBackward (Node \*list) {
  
        if (list == null) return;
  
  
        printBackward (list->next);
  
        cout << list->cargo;
  
    }
  
  

Looking at the two function calls, we have to remember that printBackward treats its argument as a list and print treats its argument as a single object.

Always keep in mind the **fundamental ambiguity theorem**:

A variable that refers to a node might treat the node as a single object or as the first in a list of nodes.

  

### 18.7 Object methods for nodes

You might have wondered why printList and printBackward are class methods. I have made the claim that anything that can be done with class methods can also be done with object methods; it's just a question of which form is cleaner.

In this case there is a legitimate reason to choose class methods. It is legal to send null as an argument to a class method, but it is not legal to invoke an object method on a null object.

    Node \*node = null;
  
    printList (node);       // legal
  
    node.printList ();      // NullPointerException
  

This limitation makes it awkward to write list-manipulating code in a clean, object-oriented style. A little later we will see a way to get around this, though.

  

### 18.8 Modifying lists

Obviously one way to modify a list is to change the cargo of one on the nodes, but the more interesting operations are the ones that add, remove, or reorder the nodes.

As an example, we'll write a method that removes the second node in the list and returns a reference to the removed node.

    Node\* removeSecond (Node \*list) {
  
        Node \*first = list;
  
        Node \*second = list->next;
  
  
        // make the first node refer to the third
  
        first->next = second->next;
  
  
        // separate the second node from the rest of the list
  
        second->next = null;
  
        return second;
  
    }
  

Again, I am using temporary variables to make the code more readable. Here is how to use this method.

        printList (node1);
  
        Node \*removed = removeSecond (node1);
  
        printList (removed);
  
        printList (node1);
  

The output is

(1, 2, 3)           the original list
  
(2)                 the removed node
  
(1, 3)              the modified list
  

Here is a state diagram showing the effect of this operation.

![](images/list5.png)

What happens if we invoke this method and pass a list with only one element (a **singleton**)? What happens if we pass the empty list as an argument? Is there a precondition for this method?

  

### 18.9 Wrappers and helpers

For some list operations it is useful to divide the labor into two methods. For example, to print a list backwards in the conventional list format, (3, 2, 1) we can use the printBackwards method to print 3, 2, but we need a separate method to print the parentheses and the first node. We'll call it printBackwardNicely.

    void printBackwardNicely (Node \*list) {
  
        cout << '(';
  
  
        if (list != null) {
  
            Node \*head = list;
  
            Node \*tail = list->next;
  
            printBackward (tail);
  
            cout << head->cargo;
  
        }
  
        cout << ')';
  
    }
  

Again, it is a good idea to check methods like this to see if they work with special cases like an empty list or a singleton.

Elsewhere in the program, when we use this method, we will invoke printBackwardNicely directly and it will invoke printBackward on our behalf. In that sense, printBackwardNicely acts as a **wrapper**, and it uses printBackward as a helper.

  

### 18.10 The LinkedList class

There are a number of subtle problems with the way we have been implementing lists. In a reversal of cause and effect, I will propose an alternative implementation first and then explain what problems it solves.

First, we will create a new class called LinkedList. Its instance variables are an integer that contains the length of the list and a reference to the first node in the list. LinkedList objects serve as handles for manipulating lists of Node objects.

class LinkedList {
  
  
  public:
  
    int length;
  
    Node\* head;
  
  
    LinkedList () {
  
        length = 0;
  
        head = null;
  
    }
  
};
  

One nice thing about the LinkedList class is that it gives us a natural place to put wrapper functions like printBackwardNicely, which we can make an object method in the LinkedList class.

    public void printBackward () {
  
        cout << '(';
  
  
        if (head != null) {
  
            Node \*tail = head->next;
  
            Node.printBackward (tail);
  
            cout << head->cargo;
  
        }
  
        cout << ')';
  
    }
  

Just to make things confusing, I renamed printBackwardNicely. Now there are two methods named printBackward: one in the Node class (the helper) and one in the LinkedList class (the wrapper). In order for the wrapper to invoke the helper, it has to identify the class explicitly (Node.printBackward).

So, one of the benefits of the LinkedList class is that it provides a nice place to put wrapper functions. Another is that it makes it easier to add or remove the first element of a list. For example, addFirst is an object method for LinkedLists; it takes an int as an argument and puts it at the beginning of the list.

    void addFirst (int i) {
  
      Node \*node = new Node (i, head);
  
      head = node;
  
      length++;
  
    }
  

As always, to check code like this it is a good idea to think about the special cases. For example, what happens if the list is initially empty?

  

### 18.11 Invariants

Some lists are "well-formed;" others are not. For example, if a list contains a loop, it will cause many of our methods to crash, so we might want to require that lists contain no loops. Another requirement is that the length value in the LinkedList object should be equal to the actual number of nodes in the list.

Requirements like this are called **invariants** because, ideally, they should be true of every object all the time. Specifying invariants for objects is a useful programming practice because it makes it easier to prove the correctness of code, check the integrity of data structures, and detect errors.

One thing that is sometimes confusing about invariants is that there are some times when they are violated. For example, in the middle of addFirst, after we have added the node, but before we have incremented length, the invariant is violated. This kind of violation is acceptable; in fact, it is often impossible to modify an object without violating an invariant for at least a little while. Normally the requirement is that every method that violates an invariant must restore the invariant.

If there is any significant stretch of code in which the invariant is violated, it is important for the comments to make that clear, so that no operations are performed that depend on the invariant.

  

### 18.12 Glossary

list
:   A data structure that implements a collection using a sequence of linked nodes.

node
:   An element of a list, usually implemented as an object that contains a reference to another object of the same type.

cargo
:   An item of data contained in a node.

link
:   An object reference embedded in an object.

generic data structure
:   A kind of data structure that can contain data of any type.

precondition
:   An assertion that must be true in order for a method to work correctly.

invariant
:   An assertion that should be true of an object at all times (except maybe while the object is being modified).

wrapper method
:   A method that acts as a middle-man between a caller and a helper method, often offering an interface that is cleaner than the helper method's.
