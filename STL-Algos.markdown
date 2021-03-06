# 105 STL Algorithms in Less Than an Hour
https://www.youtube.com/watch?v=bFSnXNIsK4A&t=1040s
CppCon 2018 SPEAKER: Jonathan Boccara

[The World Map of C++ STL Algorithms](http://www.fluentcpp.com/getTheMap/)

## 7 families of algorithms:
* the queriers,
* the permutationers,
* the algos on sets,
* the movers,
* the value modifiers,
* the structure changers,
* and the algos of raw memory.

## HEAP
* **std::make_heap**
	template <class RandomAccessIterator, class Compare>
	 void make_heap (RandomAccessIterator first, RandomAccessIterator last,
	  Compare comp );
	std::vector<int> v(10,20,30,5,15);
	std::make_heap (v.begin(),v.end());
	
* **push_heap** and 
	v.push_back(99); 
	std::push_heap (v.begin(),v.end());
	
* **pop_heap** 
	std::pop_heap (v.begin(),v.end()); 
	v.pop_back();
	
* **sort_heap**
	std::sort_heap (v.begin(),v.end());

* The standard container adaptor 
### priority_queue calls make_heap, push_heap and pop_heap automatically to maintain heap properties for a container. 
-----------------------------------------------------------------------------------------------------
## SORTING

* **std::sort**
	template <class RandomAccessIterator, class Compare>
	void sort (RandomAccessIterator first, RandomAccessIterator last, Compare comp);
	linearithmic in the distance between first and last: Performs approximately N*log2(N)
	
* **Partial_sort** 
	void partial_sort (RandomAccessIterator first, RandomAccessIterator middle,
	     RandomAccessIterator last, Compare comp);
	std::partial_sort (myvector.begin(), myvector.begin()+5, myvector.end());
	Performs approximately N*log(M) comparisons of elements (where N is this distance, 
	and M is the distance between first and middle)
	
* **nth_element**
	template <class RandomAccessIterator, class Compare>
	void nth_element (RandomAccessIterator first, RandomAccessIterator nth,
	    RandomAccessIterator last, Compare comp);
	    
* **stable_sort**
	template <class RandomAccessIterator, class Compare>
	void stable_sort ( RandomAccessIterator first, RandomAccessIterator last,
	     Compare comp );
	Performs up to N*log2(N), Performs up to N*log22(N) 
	
* **inplace_merge**
	template <class BidirectionalIterator, class Compare>
	void inplace_merge (BidirectionalIterator first, BidirectionalIterator middle,
	      BidirectionalIterator last, Compare comp);
	linear in the distance between first and last: Performs N-1 comparisons and up to twice that many element moves.

## Partitioning

* **partition** 
	BidirectionalIterator partition (BidirectionalIterator first,
			   BidirectionalIterator last, UnaryPredicate pred);
* **stable_partition**
	template <class BidirectionalIterator, class UnaryPredicate>
	BidirectionalIterator stable_partition (BidirectionalIterator first,
				  BidirectionalIterator last,
				  UnaryPredicate pred);
	This is generally implemented using an internal temporary buffer.
	
* **partition_point**
	template <class ForwardIterator, class UnaryPredicate>
	ForwardIterator partition_point (ForwardIterator first, ForwardIterator last,
			   UnaryPredicate pred);
	On average, logarithmic in the distance between first and last: Performs approximately 
	log2(N)+2 element comparisons 	(where N is this distance).
	On non-random-access iterators, the iterator advances produce themselves an additional 
	linear complexity in N on average.
	
--------------------------------------------------------

## Permutation:	

**Rotate** :
	template <class ForwardIterator>
  	ForwardIterator rotate (ForwardIterator first, ForwardIterator middle,
                          ForwardIterator last);
	
**shuffle**:
	template <class RandomAccessIterator, class URNG>
  	void shuffle (RandomAccessIterator first, RandomAccessIterator last, URNG&& g);
	
**next_permutation**:
	template <class BidirectionalIterator, class Compare>
  	bool next_permutation (BidirectionalIterator first,
                         BidirectionalIterator last, Compare comp);
			 
**prev_permutation**:
	template <class BidirectionalIterator, class Compare>
  	bool prev_permutation (BidirectionalIterator first,
                         BidirectionalIterator last, Compare comp);

**reverse**:
	template< class BidirIt >
	constexpr void reverse( BidirIt first, BidirIt last );

----------------------------------------
## is_*

**is_sorted**
	template< class ForwardIt >
	bool is_sorted( ForwardIt first, ForwardIt last );

**is_partitioned**
	template< class InputIt, class UnaryPredicate >
	bool is_partitioned( InputIt first, InputIt last, UnaryPredicate p );

**is_heap**
	template< class RandomIt >
	bool is_heap( RandomIt first, RandomIt last );

## stale_**
**stable_partition**
	template< class BidirIt, class UnaryPredicate >
	BidirIt stable_partition( BidirIt first, BidirIt last, UnaryPredicate p );
	
**stable_sort**
	template< class RandomIt >
	void stable_sort( RandomIt first, RandomIt last );

## is_*_until

**is_sorted_until**
	template< class ForwardIt >
	ForwardIt is_sorted_until( ForwardIt first, ForwardIt last );

**is_partitioned_until**
	template< class InputIt, class UnaryPredicate >
	bool is_partitioned( InputIt first, InputIt last, UnaryPredicate p );

**is_heap_until**
	template< class RandomIt >
	RandomIt is_heap_until( RandomIt first, RandomIt last );

----------------------------------------------------------------

## Numeric Algorithms
count




































