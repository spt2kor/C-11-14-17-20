# 105 STL Algorithms in Less Than an Hour
https://www.youtube.com/watch?v=bFSnXNIsK4A&t=1040s
CppCon 2018 SPEAKER: Jonathan Boccara

## HEAP
  	**std::make_heap**
		template <class RandomAccessIterator, class Compare>
 		 void make_heap (RandomAccessIterator first, RandomAccessIterator last,
                  Compare comp );
		std::vector<int> v(10,20,30,5,15);
    		std::make_heap (v.begin(),v.end());
  	**push_heap** and 
    		v.push_back(99); 
    		std::push_heap (v.begin(),v.end());
  	**pop_heap** 
    		std::pop_heap (v.begin(),v.end()); 
    		v.pop_back();
	**sort_heap**
  		std::sort_heap (v.begin(),v.end());

  	The standard container adaptor 
  	priority_queue calls 
    
## make_heap, push_heap and pop_heap automatically to maintain heap properties for a container. ##
-----------------------------------------------------------------------------------------------------
## SORTING

	**std::sort**
		template <class RandomAccessIterator, class Compare>
  		void sort (RandomAccessIterator first, RandomAccessIterator last, Compare comp);
		linearithmic in the distance between first and last: Performs approximately N*log2(N)
	**Partial_sort** 
  		void partial_sort (RandomAccessIterator first, RandomAccessIterator middle,
                     RandomAccessIterator last, Compare comp);
  		std::partial_sort (myvector.begin(), myvector.begin()+5, myvector.end());
		Performs approximately N*log(M) comparisons of elements (where N is this distance, 
		and M is the distance between first and middle)
	**nth_element**
		template <class RandomAccessIterator, class Compare>
  		void nth_element (RandomAccessIterator first, RandomAccessIterator nth,
                    RandomAccessIterator last, Compare comp);
	**stable_sort**
		template <class RandomAccessIterator, class Compare>
  		void stable_sort ( RandomAccessIterator first, RandomAccessIterator last,
                     Compare comp );
		Performs up to N*log2(N), Performs up to N*log22(N) 
	**inplace_merge**
		template <class BidirectionalIterator, class Compare>
  		void inplace_merge (BidirectionalIterator first, BidirectionalIterator middle,
                      BidirectionalIterator last, Compare comp);
		linear in the distance between first and last: Performs N-1 comparisons and up to twice that many element moves.
		
## Partitioning
	**partition** 
  		BidirectionalIterator partition (BidirectionalIterator first,
                                   BidirectionalIterator last, UnaryPredicate pred);
	**stable_partition**
		template <class BidirectionalIterator, class UnaryPredicate>
  		BidirectionalIterator stable_partition (BidirectionalIterator first,
                                          BidirectionalIterator last,
                                          UnaryPredicate pred);
		This is generally implemented using an internal temporary buffer.
	**partition_point**
		template <class ForwardIterator, class UnaryPredicate>
  		ForwardIterator partition_point (ForwardIterator first, ForwardIterator last,
                                   UnaryPredicate pred);
		On average, logarithmic in the distance between first and last: Performs approximately 
		log2(N)+2 element comparisons 	(where N is this distance).
		On non-random-access iterators, the iterator advances produce themselves an additional 
		linear complexity in N on average.
--------------------------------------------------------
## Permutation:	
	**ROtate** :
	
	__shuffle__:
	
	###next_permutation:
	
	**prev_permutation**:





















