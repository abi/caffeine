## Bugs

1. Undefined symbols (*by far* the #1)
2. Using strings as integer (forgetting to do parseInt) and a whole class of bugs due to JavaScript's weak typing
discipline and automatic casting of Strings to Numbers and vice versa.
3. Wrong number of argument or mismatched argument position.

## Wants

Wants are very secondary to bugs in terms of priorities but proper fixing of some bugs might imply the implementation
of certain wants. 

1. Haskell-like parametric polymorphism
        
2. Contracts - useful for run-time argument and return value checking. Also, useful as properties for QuickCheck-like
   testing system.
   
3. Pattern matching based on values like in Haskell.

4. Function overloading (enforced by a compiler)
    
    In Coffee currently (as in JS), you can do 
    
    ```coffee
    poly = (x) ->
        if typeof x is 'object' then do something
        if typeof x is 'string' then do something
    ```
    
    A possible nicer syntax is:
    
    ```coffee 
    poly object = ...
    poly string = ...
    ```
    
    This pattern is very common in popular libraries such as jQuery, where functions like `val` are overloaded to act as
    both getters and setters.