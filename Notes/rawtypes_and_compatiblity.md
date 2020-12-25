# Compatibility 


<hr>
<a href="../README.md">&lt;&lt; README </a>
<hr>


--------------------
### _what is Migration Compatibility ?_
- it means you can upgrade to a new version, and your code will not break

#### _Binary Compatibility for Generics :_
- you can replace a legacy class file with a generic class file without changing or recompiling any client code
    - **client code** : code that link or make use of this class
    
--------------------------



## <u>Raw Types</u>
- _a type that exists only to provide compatibility with legacy code_
- _a generic type that does not have any generic parameters_
  

- example :
    - List (without <--->)
    

- raw types can introduce unsafe scenarios into our code that causes runtime errors
    - you can assign from any generic type to a raw type or from any raw to generic
    
---------
-----------------

## <u>Erasure</u>
- what is erasure ?
    - translation at compile time not runtime
        - the generics only exist in the source code but get erase  when translated to bite code
    
---
- erasure contain three steps :
    1. _Erase type parameters_ :
        - remove the generics and look at the specific rules for what things got converted to
    2. _add cast_
        - when it is possible to pass something with different type
    3. _add bridge methods_ 
        -  When compiling a class or interface that extends a parameterized class or implements a parameterized interface, the compiler may need to create a synthetic method, called a bridge method, as part of the type erasure process
        - It's a method that allows a class extending a generic class or implementing a generic interface (with a concrete type parameter) to still be used as a raw type.
    

- Examples of Erasure:
    - List<String> >>> List
    - List<String>[] >> List[]
    - T without bounds >>> Object
    - T extends Cls >>> Cls
   

- Trade-offs of Erasure :
    - _**overloading**_:
      - can not overload a method by another if the only different is in the generic type
        - you can not overload a method that takes (list<Integer>) by a method that takes (list<String>)
            - cause both methods have the same erasure
        
    - _**checking the type of an instance**_
      - illegal to have generic type parameter when using `instanceof`
        - Obj instanceof Cls<T> >>> Wrong
            - cause at runtime this class does not really exist
        - can not declare generic exceptions(or anything you can `throw`)
            - because they are used in runtime
    - performance
        - erasure stop us from using primitive types for an array and force us to use a boxed type (ex. Integer)
            - for example :
                - an array of Integers in worst case is 8 time bigger than array of ints
----
----

## <u>reifiable Types and arrays</u>
- to create a generic array :
    - `T[] arr = (T[]) new Object[size];`
    - or you can just leave it as array of objects and cast the elements of the array when you use them
    
--------

<hr>
<a href="../README.md">&lt;&lt; README </a>
<hr>
    


    
    
