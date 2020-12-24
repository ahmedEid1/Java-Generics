<hr>
<a href="../README.md">&lt;&lt; README </a>
<hr>

# <u>Generics With Collections</u>

- collections are the most common use of Generics

### List(ordered, ex. ArrayList) : 
- List is a generic interface `List<>` and its implementations are generic classes (ex. `ArrayList<>`)


-----

### Set(unique, ex. HashSet) : 
- Set is a generic interface `Set<>` and its implementations are generic classes (ex. `HashSet<>`)

- sets do not have order
- can check if element is in the set using `contains`

-----------

### Map(pairs of keys and values, ex. HashMap) : 
- Map is a generic interface `Map<k, v>` and its implementations are generic classes (ex. `HashMap<>`)
- keys are unique
- Map.Entry<k, v> is also generic ()



-----
### the problem with arrays :

1. no easy `toString` implementation 
    - need to use the static class `Arrays`.toString(arr)
    

 2. not resizable 
    - need to copy the array to a bigger array then add a new element 
        - `Arrays.copyOf(oldArr, new_length)`
    

3. do not have many methods that add functionality 

-------------

### <u>the diamond operator <></u> :
- Def. :
    - do not add the generic in explicitly just infer(i.e. conclude) it from the context
    
- example :
    -   `List<Person> myList = new ArrayList<>();`
    
------

- _iterator is a generic interface_
- _you can have as many parameters in generic class as many as you need to (there is no hard limit)_
    - _but it is recommended not to go over two or three_
-------------


<hr>
<a href="../README.md">&lt;&lt; README </a>
<hr>