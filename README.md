# <u>Generics</u>

-------------
<ol>
<li>

[Collections and Generics](Notes/generic_collections.md)
</li>
<li>

[classes & interfaces and Generics](Notes/classes_and_interfaces.md)
</li>
<li>

[Generics on Methods](Notes/generics_on_methods.md)
</li>
<li>

[Wildcard on Generics](Notes/wildcard_generics.md)
</li>
<li>

[Generics Compatibility](Notes/rawtypes_and_compatiblity.md)
</li>
<li>

[Generics and reflection](Notes/reflections.md)
</li>
<li>

[advance topics](Notes/advance.md)
</li>

</ol>

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
<ol>
<li>

[Collections and Generics](Notes/generic_collections.md)
</li>
<li>

[classes & interfaces and Generics](Notes/classes_and_interfaces.md)
</li>
<li>

[Generics on methods](Notes/generics_on_methods.md)
</li>
<li>

[Wildcard on Generics](Notes/wildcard_generics.md)
</li>
<li>

[Generics Compatibility](Notes/rawtypes_and_compatiblity.md)
</li>
<li>

[Generics and reflection](Notes/reflections.md)
</li>
<li>

[advance topics](Notes/advance.md)
</li>
</ol>

--------



    