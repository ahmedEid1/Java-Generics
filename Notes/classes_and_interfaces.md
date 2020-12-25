# <u>Generics and inheritance</u>
###### How do Generics interact with inheritance ?
<hr>
<a href="../README.md">&lt;&lt; README </a>
<hr>

-------

### <u>implementing a Generic type</u>
- Example :
    - implementing a Generic interface :
        - `public class PersonComparator implement Comparator<Person> {`
            - `Comparator` is raw type, and you need to make it properly instantiated generic type (i.e. adding \<specific type>) 
 ---

### <u>passing parameters to a Generic type</u>
- Example :
    - creating a  ReverseComparator that take another Comparator and reverse its sort order
        - but we need this done in type safe way :
          
            - `public class ReverseComparator<T> implement Comparator<T> {`
                - `private Comparator OriginalComparator<T>;`
                - `public ReverseComparator(Comparator<T> OriginalComparator){`
                    - `this.OriginalComparator = OriginalComparator;`
                - `}`
                - `public int compare(T O1, T O2){`
                    - `return -1 * OriginalComparator.compare(O1, O2);`
                - `}`
            - `}`
        -     ReverseComparator<T> pass the the type parameters up to Comparator<Person>
    
-----------------

### <u>Type Bounds</u>
- restricting my type by a bound
    - **for example :**
        - I want the type to know what is its sort order is (i.e. implement the Comparable interface) 
            - `MyClass<T extends Comparable<T>>`
    
------

### what is the goal of generics ?
- `type safety without code duplication`

--------------
<hr>
<a href="../README.md">&lt;&lt; README </a>
<hr>
    


