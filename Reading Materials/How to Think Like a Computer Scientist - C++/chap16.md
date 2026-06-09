---
title: "Chapter 16: Pointers and References"
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

# Chapter 16: Pointers and References

> Recovered from eckenrodehouse.net via the Wayback Machine. Part of [[How to Think Like a Computer Scientist - C++]].

---

# Pointers and References

\author{Paul Bui}

I suppose the easiest way to explain pointers and references is to jump right into an example. Let's first take a look at some Algebra:

| x = 1 |

In Algebra, when you use a variable, it is essentially a letter or designation that you use to store some number. In programming, the variable in the equation above must be on the left side. You've probably noticed by now that the compiler won't let you do something like this:

1 = x;
  

And if you didn't know this...now you know, and knowing is half the battle. The reason why you receive a compile-time error like "lvalue required in..." is because the left hand side of the equation, traditionally referred to as the **lvalue**, must be an address in memory. Think about it for a second. If you wanted to store some data somewhere, you first need to know where you're going to store it before the action can take place. The **lvalue** is the address of the place in memory where you're going to store the information and/or data of the right hand side of the equation, better known as the **rvalue**.

In C++, you will most likely at one point or another, deal with memory management. To manipulate addresses, C++ has two mechanisms: **pointers** and **references**.

  

### 16.1 What are pointers and references?

Pointers and references are essentially variables that hold memory addresses as their values. You learned before about the various different data types such as: int, double, and char. Pointers and references hold the addresses in memory of where you find the data of the various data types that you have declared and assigned. The two mechanisms, pointers and references, have different syntax and different traditional uses.

  

### 16.2 Declaring pointers and references

When declaring a pointer to an object or data type, you basically follow the same rules of declaring variables and data types that you have been using, only now, to declare a pointer of SOMETYPE, you tack on an asterix \* between the data type and its variable.

SOMETYPE\* sometype;
  
  
int\* x;
  

To declare a reference, you do the exact same thing you did to declare a pointer, only this time, rather than using an asterix \*, use instead an ampersand &.

SOMETYPE& sometype;
  
  
int& x;
  

As you probably have already learned, spacing in C++ does not matter, so the following pointer declarations are identical:

SOMETYPE\*  sometype;
  
SOMETYPE \* sometype;
  
SOMETYPE  \*sometype;
  

The following reference declarations are identical as well:

SOMETYPE&  sometype;
  
SOMETYPE & sometype;
  
SOMETYPE  &sometype;
  
  

### 16.3 The "address of" operator

Although declaring pointers and references look similar, assigning them is a whole different story. In C++, there is another operator that you'll get to know intimately, the "address of" operator, which is denoted by the ampersand & symbol. The "address of" operator does exactly what it says, it returns the "address of" a variable, a symbolic constant, or a element in an array, in the form of a pointer of the corresponding type. To use the "address of" operator, you tack it on in front of the variable that you wish to have the address of returned.

SOMETYPE\* x = &sometype; // must be used as rvalue
  

Now, do not confuse the "address of" operator with the declaration of a reference. Because use of operators is restricted to rvalues, or to the right hand side of the equation, the compiler knows that &SOMETYPE is the "address of" operator being used to denote the return of the address of SOMETYPE as a pointer.

Furthermore, if you have a function which has a pointer as an argument, you may use the "address of" operator on a variable to which you have not already set a pointer to point. By doing this, you do not necessarily have to declare a pointer just so that it is used as an argument in a function, the "address of" operator returns a pointer and thus can be used in that case too.

SOMETYPE MyFunc(SOMETYPE \*x)
  
{
  
  cout << \*x << endl;
  
}
  
  
int main()
  
{
  
  SOMETYPE i;
  
  
  MyFunc(&i);
  
  
  return 0;
  
}
  
  

### 16.4 Assigning pointers and references

As you saw in the syntax of using the "address of" operator, a pointer is assigned to the return value of the "address of" operator. Because the return value of an "address of" operator is a pointer, everything works out and your code should compile. To assign a pointer, it must be given an address in memory as the rvalue, else, the compiler will give you an error.

int x;
  
int\* px = &x;
  

The above piece of code shows a variable x of type int being declared, and then a pointer px being declared and assigned to the address in memory of x. The pointer px essentially "points" to x by storing its address in memory. Keep in mind that when declaring a pointer, the pointer needs to be of the same type pointer as the variable or constant from which you take the address.

Now here is where you begin to see the differences between pointers and references. To assign a pointer to an address in memory, you had to have used the "address of" operator to return the address in memory of the variable as a pointer. A reference however, does not need to use the "address of" operator to be assigned to an address in memory. To assign an address in memory of a variable to a reference, you just need to use the variable as the rvalue.

int x;
  
int& rx = x;
  

The above piece of code shows a variable x of type int being declared, and then a reference rx being declared and assigned to "refer to" x. Notice how the address of x is stored in rx, or "referred to" by rx without the use of any operators, just the variable. You must also follow the same rule as pointers, wherein you must declare the same type reference as the variable or constant to which you refer.

Hypothetically, if you wanted to see what output a pointer would be...

#include <iostream.h>
  
  
int main()
  
{
  
  int someNumber = 12345;
  
  int\* ptrSomeNumber = &someNumber;
  
  
  cout << "someNumber = " << someNumber << endl;
  
  cout << "ptrSomeNumber = " << ptrSomeNumber << endl;
  
  
  return 0;
  
}
  

If you compiled and ran the above code, you would have the variable someNumber output 12345 while ptrSomeNumber would output some hexadecimal number (addresses in memory are represented in hex). Now, if you wanted to cout the value pointed to by ptrSomeNumber, you would use this code:

#include <iostream.h>
  
  
int main()
  
{
  
  int someNumber = 12345;
  
  int\* ptrSomeNumber = &someNumber;
  
  
  cout << "someNumber = " << someNumber << endl;
  
  cout << "ptrSomeNumber points to " << \*ptrSomeNumber << endl;
  
  
  return 0;
  
}
  

So basically, when you want to use, modify, or manipulate the value pointed to by pointer x, you denote the value/variable with \*x.

Here is a quick list of things you can do with pointers and references:

- You can assign pointers to "point to" addresses in memory
- You can assign references to "refer to" variables or constants
- You can copy the values of pointers to other pointers
- You can modify the values stored in the memory pointed to or referred to by pointers and/or references, respectively
- You can also increment or decrement the addresses stored in pointers
- You can pass pointers and/or references to functions (Further information on "Passing by reference" can be found HERE)

  

### 16.5 The Null pointer

Remember how you can assign a character or string to be **null**? If you don't remember, check out HERE. The **null** character in a string denotes the end of a string, however, if a pointer were to be assigned to the null pointer, it points to nothing. The null pointer is often denoted by 0 or null. The null pointer is often used in conditions and/or in logical operations.

#include <iostream.h>
  
  
int main()
  
{
  
  int x = 12345;
  
  int\* px = &x;
  
  
  while (px) {
  
    cout << "Pointer px points to something\n";
  
    px = 0;
  
  }
  
  
  cout << "Pointer px points to null, nothing, nada!\n";
  
  
  return 0;
  
}
  

If pointer px is NOT null, then it is pointing to something, however, if the pointer is null, then it is pointing to nothing. The null pointer becomes very useful when you must test the state of a pointer, whether it has a value or not.

  

### 16.6 Dynamic Memory Allocation

You have probably wondered how programmers allocate memory efficiently without knowing, prior to running the program, how much memory will be necessary. Here is when the fun starts with dynamic memory allocation.

Several sections ago, we learned about assigning pointers using the "address of" operator because it returned the address in memory of the variable or constant in the form of a pointer. Now, the "address of" operator is NOT the only operator that you can use to assign a pointer. In C++ you have yet another operator that returns a pointer, which is the **new** operator. The new operator allows the programmer to allocate memory for a specific data type, struct, class, etc, and gives the programmer the address of that allocated sect of memory in the form of a pointer. The new operator is used as an rvalue, similar to the "address of" operator. Take a look at the code below to see how the new operator works.

int n = 10;
  
SOMETYPE \*parray, \*pS;
  
int \*pint;
  
  
parray = new SOMETYPE[n];
  
pS = new SOMETYPE;
  
pint = new int;
  

By assigning the pointers to an allocated sect of memory, rather than having to use a variable declaration, you basically override the "middleman" (the variable declaration. Now, you can allocate memory dynamically without having to know the number of variables you should declare. If you looked at the above piece of code, you can use the new operator to allocate memory for arrays too, which comes quite in handy when we need to manipulate the sizes of large arrays and or classes efficiently. The memory that your pointer points to because of the new operator can also be "deallocated," not destroyed but rather, freed up from your pointer. The delete operator is used in front of a pointer and frees up the address in memory to which the pointer is pointing.

delete parray;
  
delete pint;
  

The memory pointed to by parray and pint have been freed up, which is a very good thing because when you're manipulating multiple large arrays, you try to avoid losing the memory someplace by leaking it. Any allocation of memory needs to be properly deallocated or a leak will occur and your program won't run efficiently. Essentially, every time you use the new operator on something, you should use the delete operator to free that memory before exiting. The delete operator, however, not only can be used to delete a pointer allocated with the new operator, but can also be used to "delete" a null pointer, which prevents attempts to delete non-allocated memory (this actions compiles and does nothing).

The new and delete operators do not have to be used in conjunction with each other within the same function or block of code. It is proper and often advised to write functions that allocate memory and other functions that deallocate memory.

  

### 16.7 Returning pointers and/or references from functions

When declaring a function, you must declare it in terms of the type that it will return, for example:

int MyFunc(); // returns an int
  
SOMETYPE MyFunc(); // returns a SOMETYPE
  
  
int\* MyFunc(); // returns a pointer to an int
  
SOMETYPE \*MyFunc(); // returns a pointer to a SOMETYPE
  
SOMETYPE &MyFunc(); // returns a reference to a SOMETYPE
  
  

Woah, my a-paul-igies, I didn't mean to jump right into it, but I'm pretty sure that if you're understanding pointers, the declaration of a function that returns a pointer or a reference should seem relatively logical. The above piece of code shows how to basically declare a function that will return a reference or a pointer.

SOMETYPE \*MyFunc(int \*p)
  
{
  
   ...
  
   ...
  
   return p;
  
}
  
  
SOMETYPE &MyFunc(int &r)
  
{
  
  ...
  
  ...
  
  return r;
  
}
  

Within the body of the function, the return statement should NOT return a pointer or a reference that has the address in memory of a local variable that was declared within the function, else, as soon as the function exits, all local variables ar destroyed and your pointer or reference will be pointing to some place in memory that you really do not care about. Having a dangling pointer like that is quite inefficient and dangerous outside of your function.

However, within the body of your function, if your pointer or reference has the address in memory of a data type, struct, or class that you dynamically allocated the memory for, using the new operator, then returning said pointer or reference would be reasonable.

SOMETYPE \*MyFunc()  //returning a pointer that has a dynamically
  
{           //allocated memory address is proper code
  
   int \*p = new int[5];
  
   ...
  
   ...
  
   return p;
  
}
  
  

### 16.8 Glossary

pointer
:   a variable that holds an address in memory. Similar to a reference, however, pointers have different syntax and traditional uses from references.

reference
:   a variable that holds an address in memory. Similar to a pointer, however, references have different syntax and traditional uses from pointers.

"address of" operator
:   an operator that returns the address in memory of a variable.

dynamic memory allocation
:   the explicit allocation of contiguous blocks of memory at any time in a program.

new
:   an operator that returns a pointer of the appropriate data type, which points to the reserved place.

delete
:   an operator that returns the memory pointed to by a pointer to the free store (a special pool of free memory that each program has)
