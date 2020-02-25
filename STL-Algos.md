# 105 STL Algorithms in Less Than an Hour
https://www.youtube.com/watch?v=bFSnXNIsK4A&t=1040s
CppCon 2018 SPEAKER: Jonathan Boccara

  std::make_heap
    std::vector<int> v(10,20,30,5,15);
    std::make_heap (v.begin(),v.end());
  push_heap and 
    v.push_back(99); 
    std::push_heap (v.begin(),v.end());
  pop_heap 
    std::pop_heap (v.begin(),v.end()); 
    v.pop_back();
sort_heap
  std::sort_heap (v.begin(),v.end());

  The standard container adaptor 
  priority_queue calls 
    make_heap, push_heap and pop_heap automatically to maintain heap properties for a container.































