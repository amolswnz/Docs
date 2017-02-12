####What is difference between class and interface?
 1. Interfaces do not contain business logic 
 2. You must extend interface to use.
 3. You can't create object of interface.

####How to call parent constructor?
 parent::__construct()

####There are 3 types of visibility of method & property and are following
 Public: Can be accessed from same class method, child class and from outside of class.<br>
 Protected : Can be accessed from same class method, child class.<br>
 Private: Can be accessed from same class method only.<br> 

####What is Abstraction in PHP?
####Abstract is 
 1. Classes defined as abstract may not be instantiated
 2. To extend the Abstract class, extends operator is used.
 3. You can inherit only one abstract class at one time extending.
 4. they can't define the implementation.
 5. declaration must be defined by the child.
 6. number of parameter must be match between parent & child class.

####What is Interface in PHP?
####Interface is a pattern
 1. All methods declared in an interface must be public
 2. Classes defined as Interface may not be instantiated (create object).
 3. To extend the interface class, implements operator is used.
 4. You can inherit any number of interface class seperated by comma
 5. All methods in the interface must be implemented within a child class; failure to do so will result in a fatal error.
 6. number of parameter must be match between parent & child class.

####Interface vs Abstaction
 1. Abstract no body
 2. Abstract private public protected
 3. Interface only public
 4. Abstract cannot extend another abstract
 5. Child only one abstract
 6. Child many interfaces

