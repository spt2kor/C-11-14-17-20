[Automatic Memory Management of the STL Containers](https://www.modernescpp.com/index.php/automatic-memory-management-with-containers)
# Automatic Memory Management of the STL Containers

### std::string and std::vector
1.  The adjustment of the size and the capacity of the container is done automatically. I haven't used any kind of memory operations like new and delete.
2.  std::string and std::vector support the same interface. The only exception to this rule is line 41. Here I added a C string to a C++ string.
3.  By using the method cont.resize(n) the container cont will get new default-initialized elements, if n > cont.size() is true.
4.  By using the method cont.reserve(n) the container cont will be get new memory for at least n elements, if n > cont.capacity() is true.
4.  The call shrink_to_fit is non-binding. That means, the C++ runtime has not to adjust the capacity of a container to its size. But, my usages of the method shrink_to_fit with GCC, clang, or cl.exe always freed the unnecessary memory.


------------------------------------------------------
# [The SoA Vector – Part 1: Optimizing the Traversal of a Collection](https://www.fluentcpp.com/2018/12/18/the-soa-vector-part-1-optimizing-the-traversal-of-a-collection/)


# [The SoA Vector – Part 2: Implementation in C++](https://www.fluentcpp.com/2018/12/21/an-soa-vector-with-an-stl-container-interface-in-cpp/)

Proxy types
The iterator class

---------------------------------
# [Understanding the STL](http://www.fluentcpp.com/STL/)











