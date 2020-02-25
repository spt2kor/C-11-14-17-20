# Why is std::rotate so fast?
[why-is-stdrotate-so-fast](https://stackoverflow.com/questions/21160875/why-is-stdrotate-so-fast)

```
template <class ForwardIterator>
void rotate (ForwardIterator first, ForwardIterator middle, ForwardIterator last)
{
  ForwardIterator next= middle;

  while (first != next)
  {
	swap (*first++, *next++);

	if(next == last)
		next= middle;
	else if (first==middle)
		middle= next;
  }
}
```

https://github.com/apple/swift-evolution/blob/master/proposals/0078-rotate-algorithm.md
* The C++ implementation of the rotate algorithm for the ForwardIterator (ForwardIndex in Swift) may look like this:
* The C++ implementation of the rotate algorithm for the BidirectionalIterator
* The C++ implementation of the rotate algorithm for the RandomAccessIterator

[Method 4 (The Reversal Algorithm) ](https://www.geeksforgeeks.org/program-for-array-rotation-continued-reversal-algorithm/)
* Reverse A to get ArB, where Ar is reverse of A.
* Reverse B to get ArBr, where Br is reverse of B.
* Reverse all to get (ArBr) r = BA.


[ Program for array rotation ](https://www.geeksforgeeks.org/array-rotation/)
* METHOD 1 (Using temp array) :  	Time complexity : O(n) Auxiliary Space : O(d)
* METHOD 2 (Rotate one by one) : 	Time complexity : O(n * d)  : Auxiliary Space : O(1)
* METHOD 3 (A Juggling Algorithm): 	Time complexity : O(n)  : Auxiliary Space : O(1) 	: using GCD - IMP

[Block swap algorithm for array rotation](https://www.geeksforgeeks.org/block-swap-algorithm-for-array-rotation/)
	Initialize A = arr[0..d-1] and B = arr[d..n-1]
	1) Do following until size of A is equal to size of B
	  a)  If A is shorter, divide B into Bl and Br such that Br is of same 
	       length as A. Swap A and Br to change ABlBr into BrBlA. Now A
	       is at its final place, so recur on pieces of B.  
	   b)  If A is longer, divide A into Al and Ar such that Al is of same 
	       length as B Swap Al and B to change AlArB into BArAl. Now B
	       is at its final place, so recur on pieces of A.
	2)  Finally when A and B are of equal size, block swap them.
