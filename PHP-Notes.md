#Singleton
    Single object instance during the runtime or at any time during the execution of the application
    eg. Database connection, session

#Inheritance
    extends SuperClassName

    parent::__construct

#Magic methods
    __get()
    __set()
    __isset()
    __unset()
    __sleep()   - Serialize object
    __wake()    - Unseriazlie object

#Traits
    trait TraitName  // Trait defination

    use TraitName   // Usage in classes
    use TraitName { methodName or propertyName as protected/private; ...}

#Abstract 
    abstract class ClassName    // Defination 
    Abstract Classes cannot be instatiated
    Abstract Classes 
        Serve as a superclass defination / template
        Foundation / Starting point for a class
    Abstract Methods 
        No implementation
        Subclass must have the implementation
        If any method is marked as abstract the class should also be abstract

#Interfaces
    interface InterfaceName // Defination
    Base class implements InterfaceName

#Type hinting
    Strongly typed varibles - int string float boolean etc
    declare(strict_types=1); // Add this on top of file to implement strong type hinting
    defining 
        functionName(string $var) : string // : string is return type



ALTER TABLE `oophp`.`am_users`   
  CHANGE `createdAt` `createdAt` TIMESTAMP DEFAULT NOW(),
  CHANGE `updatedAt` `updatedAt` TIMESTAMP DEFAULT NOW() ON UPDATE NOW();
