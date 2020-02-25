# Why is std::rotate so fast?
[why-is-stdrotate-so-fast](https://stackoverflow.com/questions/21160875/why-is-stdrotate-so-fast)

,,,
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
,,,














