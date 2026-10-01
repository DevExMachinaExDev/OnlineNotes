# Std::Vector

std::vector is part of the C++ standard library.

Is a dynamically resizing array. This means that it holds all of its members contiguously in memory and will resize when its capacity is reached and more items are attempted to be added to it. This usually means moving the entire array over to a new memory location. The new size of the array is dependent on the compiler and therefore if relevant it should be defined by the programmer. 

It should be noted that reallocation destroys all pointers to the vector which can create issues so regulating size when pointers are involved is important.

They should also be noted that insertion in the center of the vector is O(n) time because it needs to move over all of the elements to accommodate.

Some important notes for performance are that you should try and allocate the entire arraysize before use if possible.

Another thing is that if you initialise the array with 

```
std::vector<int> v;
v.reserve(100);
```

This does not have to run through all the array once setting all the values to 0 but that memory may already store everything where as if you do it with:

```
std::vector<int> v(100);
```

It has to set everything to 0 with a loop through the vector before use but you have guaranteed initialised values. Often using reserve and pushing back is the better option.


Vectors are highly useful for speed due to their cache friendliness, widespread use and flexibility.