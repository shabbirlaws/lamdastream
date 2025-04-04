Functional Interfaces:
---------------------
1. BiConsumer BiConsumer - java.util.function (Java Platform SE 8 ) - Oracle
2. Supplier Supplier - java.util.function (Java Platform SE 8 ) - Oracle
3. Consumer Java™ Platform Standard Ed. 8. Prev Class; Next Class ... T - the type of the input to …
4. Function Type Parameters: T - the type of the input to the function R - the type of the result of …
5. Predicate
6. BiPredicate - java.util.function (Java Platform SE 8 ) - Oracle
7. BiFunction Type Parameters: T - the type of the first argument to the function U - the type of …

Java Streams:
Different Operations On Streams
There are two types of Operations in Streams:
   Intermediate Operations
   Terminal Operations

 Intermediate Operations
 -----------------
   1. map()
    The map method is used to return a stream consisting of the results of applying the given function to the elements of this stream.
    Syntax:
    <R> Stream<R> map(Function<? super T, ? extends R> mapper)
  2. filter()
    The filter method is used to select elements as per the Predicate passed as an argument.  
    Syntax:
    Stream<T> filter(Predicate<? super T> predicate)
  3. sorted()
   The sorted method is used to sort the stream.
   Syntax:
   Stream<T> sorted()
    Stream<T> sorted(Comparator<? super T> comparator)
4.flatMap()
  Syntax:
   The flatMap operation in Java Streams is used to flatten a stream of collections into a single stream of elements.
   <R> Stream<R> flatMap(Function<? super T, ? extends Stream<? extends R>> mapper)
5. distinct ()
   Removes duplicate elements. It returns a stream consisting of the distinct elements (according to Object.equals(Object)).
   Syntax:
   Stream<T> distinct()
6. peek()
   Performs an action on each element without modifying the stream. It returns a stream consisting of the elements of this stream, additionally performing the provided action on each element as elements are consumed from the resulting stream.
   Syntax:
  Stream<T> peek(Consumer<? super T> action)

Terminal Operations
-------------------
Terminal Operations are the type of Operations that return the result. These Operations are not processed further just return a final result value.
There are a few Terminal Operations mentioned below:

1. collect()
  The collect method is used to return the result of the intermediate operations performed on the stream.
  Syntax:
  <R, A> R collect(Collector<? super T, A, R> collector)
2. forEach()
   forEach method is used to iterate through every element of the stream.
  Syntax:
  void forEach(Consumer<? super T> action)
3. reduce()
   ntax: The reduce method is used to reduce the elements of a stream to a single value. The reduce method takes a BinaryOperator as a parameter.
   T reduce(T identity, BinaryOperator<T> accumulator)
   Optional<T> reduce(BinaryOperator<T> accumulator)
4. count()
   Returns the count of elements in the stream.
   Syntax:
   long count()
5. findFirst()
   Returns the first element of the stream, if present.
   Syntax:
    Optional<T> findFirst()
6. allMatch()
  Checks if all elements of the stream match a given predicate.
  Syntax:
   boolean allMatch(Predicate<? super T> predicate)
7. anyMatch()
  Checks if any element of the stream matches a given predicate.
   Syntax:
   boolean anyMatch(Predicate<? super T> predicate)
