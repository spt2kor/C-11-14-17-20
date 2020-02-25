## [std::weak_ptr](https://www.modernescpp.com/index.php/std-weak-ptr)

## [std::shared_ptr](https://www.modernescpp.com/index.php/std-shared-ptr)

	The control block has

	a counter for the std::shared_ptr.
	a counter for the std::weak_ptr.
	eventually further data like a special deleter or an allocator.


## [Specialities of std::shared_ptr] (https://www.modernescpp.com/index.php/specialities-of-std-shared-ptr)
* First, I show with std::shared_from_this how to create a std::shared_ptr from an object; 
* second, I'm interested in the question to the answer: Should a function take a std::shared_ptr by copy or by reference? 



