# <u>Generics</u>

-------------
<ul>
<li>

[Collections and Generics](Notes/generic_collections.md)
</li>
</ul>

--------

### <u>introduction</u> 

-----
Collections can contain any Object

#### <u>example (circularBuffer)</u> 
- to ensure type safety in a circularBuffer:
    - you need to force the parameters to be of the needed type
        - which mean you need an implementation for every type you need (StringCircularBuffer, IntCircularBuffer, ....)

    
- _**problem**_ :
    - you either have unsafe code or duplicated(copy and paste) code
        - but copying and pasting several times leads to maintains errors
    - **solution** :
        - _making the CircularBuffer class generic_

--------------


### <u>Why do we need Generics ?!</u>
-  to get type safety without (copy and paste)
   - _Generics solve the conflict between type safety and boilerplate_
    - _Generics stops runtime error at compile time_

--------------

-------------
<ul>
<li>

[Collections and Generics](Notes/generic_collections.md)
</li>
</ul>

--------



    