Assumptions are an implementation that allows developments to incorporate

    assumption(truthy-expression)
    
    
into their code what, if added at the top-level, will result in this code being executed 
when the file is loaded by Node.js.  In the event of an assumption failing then an exception
is thrown which typically results in the termination of the `SLE` application with an 
associated error message and an reference to the failing assumption.
 
A second style of assumption is include in this package which compares whether or not two
JavaScript objects are equal.  This has the form

    assumptionEqual(expr1, expr2)
    
As with `assumption` this function will fail in the event that the Node.js library

    Assert.deepEqual(expr1, expr2)
    
fails otherwise the assumption will be treated as validated and processing will continue
as normal.