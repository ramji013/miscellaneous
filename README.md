# Java


****stack vs Heap memories:

for a method in a class, a frame will be created in stack.

Lets say a method m1 created in a class, a frame will be created in a stack for the same. and if the method has variable x and calling another method m2, the will be created with the above said frame and another frame will be created for m2 on top of the m1 frame.


**Heap:**

if new operator invoked, a heap memory will be created and the reference variable will be created in stack. the assignment operator will point the object in the heap.

good video explaination: https://www.youtube.com/watch?v=450maTzSIvA


**How arraylist works internally:**

Arraylist internall use array of object class to store its object.
It is resizable implementation of list interface.
The array of object class is defined as **transient object[] elementData;**

why transient
it provide a custom readObject and writeObject methods to do a better job of serialization than default.

How arraylist created:
public arraylist with initial capacity.

    

**difference between comparable and comparator**

comparable is for default nature of sorting order
comparator customized sorting order


**Comparable interface:**

1. Default natural sorting order
2. java.lang package
3. it contains, one method, compareTo method
4. all wrapper classes under string class implements comparable



**Comparator interface:**

1. Customized sorting order
2. java.util package
3. It contains 2 methods. 
    a. compare
    b. equals
4. no predefined. 2 class uses comparator
   a. collator
   b. rule based collator
   both used in gui based application
 
   

**Shallow, Deep Comparision**

**Shallow comparision:**

double equals can be used. It just check memory address of two objects.

**Deep comparision:**

It compare internal details of two objects.


**ConcurrentHashMap vs HashTable:**

ConcurrentHashMap uses multiple buckets to store data. This avoids read locks and greatly improves performance over a HashTable. Both are thread safe, but there are obvious performance wins with ConcurrentHashMap.

When you read from a ConcurrentHashMap using get(), there are no locks, contrary to the HashTable for which all operations are simply synchronized. HashTable was released in old versions of Java whereas ConcurrentHashMap is a java 5+ thing.



Functional Interface:

There are four types.
1. Predicate.  -> it return true or false based on the 2nd argument
2. Consumer.   -> it just cosume and don't produce output
3. Function.   -> it consumes request and produce output
4. Supplier.  -> it only produce output
