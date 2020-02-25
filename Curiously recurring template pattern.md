# [Curiously recurring template pattern](https://en.wikipedia.org/wiki/Curiously_recurring_template_pattern)

## [Barton–Nackman trick](https://en.wikipedia.org/wiki/Barton%E2%80%93Nackman_trick)
Barton–Nackman trick is a term coined by the C++ standardization committee (ISO/IEC JTC1/SC22 WG21) to refer to an idiom introduced by John Barton and Lee Nackman as Restricted Template Expansion.[1]
```
// A class template to express an equality comparison interface.
template<typename T> class equal_comparable {
    friend bool operator==(T const &a, T const &b) { return  a.equal_to(b); }
    friend bool operator!=(T const &a, T const &b) { return !a.equal_to(b); }
};

 // Class value_type wants to have == and !=, so it derives from
 // equal_comparable with itself as argument (which is the CRTP).
class value_type : private equal_comparable<value_type> {
  public:
    bool equal_to(value_type const& rhs) const; // to be defined
};
```

# [Use CRTP for polymorphic chaining](https://marcoarena.wordpress.com/2012/04/29/use-crtp-for-polymorphic-chaining/)


## [An Alternative to Name Injection from Templates](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/1995/N0777.pdf)

------------------------------------------------------------------------------------

# [Counting Objects in C++](https://www.drdobbs.com/cpp/counting-objects-in-c/184403484)

```
template<typename T>
class Counter {
public:
    Counter() { ++count; }
    Counter(const Counter&) { ++count; }
    ~Counter() { --count; }
 
    static size_t howMany()
    { return count; }
 
private:
    static size_t count;
};
 
template<typename T>
size_t
Counter<T>::count = 0; // this now can go in header
```


---------------------------------------------------------------




















