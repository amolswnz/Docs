#PHP 7
###New Features
* PHP6 - Due to voting the version name did not came in effect
* Type Declaration
 * int, float, bool, string
 * `declare(strict_types=1);` // Strict types checking is enabled
 * `function functionName(type $var1, type $var2) : returnType { ... }`
* Null Coalesce Operator `??`
 * PHP 5.x code <br>
    `if(isset($_GET['id']))
        $id = $_GET['id'];
    else 
        $id = 1;`
 * PHP 7.x code <br>
    `$id = $_GET['id'] ?? 1;`
* Spaceship Operator `<=>`
 * PHP 5.x code <br>
    `if($a>b)
        echo "1";
    else 
        echo "-1"`
 * PHP 7.x code <br>
    `echo $a <=> $b;`
* Splat
 * `function functionName(...$args)` // Get all the arguments as an array <br>
   `functionName($a, $b, $c, $d)`
* Grouping Use
 * PHP 5.x code <br>
    `use myNameSpace/ClassA;
    use myNameSpace/ClassB as B;
    use myNameSpace/ClassC;`
 * PHP 7.x code <br>
    `use myNameSpace/{ClassA, ClassB as B, ClassC}`
* Nullable types
 * PHP 5.x code <br>
  * `function functionName(type $var1, type $var2 = '') : returnType { ... }` 
 * PHP 7.x code <br>
  * `function functionName(type $var1, ?type $var2) : returnType { ... }` // The ? before parameter mean that it can accept `null` value
  * `echo functionName($a);` 
  * `function functionName(type $var1, type $var2) : ?returnType { ... }` // The ? before parameter mean the function can return `null` value
* Multiple `catch`
 * PHP 5.x code <br>
  * `try {
        ...
    } catch(Exception1 $e) {
        ...
    } catch(Exception2 $e) {
        ...
    } catch(Exception3 $e) {
        ...
    }`
 * PHP 7.x code <br>
  * `try {
        ...
    } catch(Exception1 | Exception2 | Exception3 $e) {
        ...
    }`
* More [http://php.net/manual/en/migration70.new-features.php]

###What's changed
* Fatal Error Catching 
 `try {
  ...
 } catch(Error $e) {
  ...
 }`
* 

 
