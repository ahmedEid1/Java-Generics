## Functional Interfaces :
##### \>>>>> wildcard Use Case


<hr>
<a href="../README.md">&lt;&lt; README </a>
<hr>


---
_- lambda expressions have types which are functional Interfaces_
    - a functional interface is:
        - _**an abstract interface with a single abstract method**_
---    
- Example :
    - `Comparator<? super Cls> `
    - the Function interface : 
        - `Function<T, R> >>>> Function<? super Cls {input}, ? extends Cls {output}>`
          
---
---

## Type inference :
- a feature that allow us to infare the type of the method parameters from _**the context**_
    

- Note :
    - when you see an error in a lambda expression related to a generic type :
        - you do not need to fix the use of generics inside the expression
            - you need to fix the use of generics in the target type       
    -  _**so, when you see an error check first that the target type is correct**_
----
----
    
## Intersection Types

- Example :
    - `<T extends A&B>`
        - T is a subtype of A and B
        
- Usage :
    - Faking a missing class or interface in badly designed API
    

- _intersection type cast_ :
    - Runnable Obj =` (Runnable & Serializable) `....
    
-------
-------
## varargs and Generics

- arguments to function that can take variable number of values (ex. `...values`)

#### what is Heap pollution ?!
- **_getting a value in your heap that is a different type from what your compiler think it should be_**

---
---
<hr>
<a href="../README.md">&lt;&lt; README </a>
<hr>


