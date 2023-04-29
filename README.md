# PHPClassTypeHintBaseOnParentClass
Class type hint base on parent class as data type

```PHP
<?php 

interface Only {
  
  public function print_result( string $test ) : string ;
    
}

interface OnlyFor {
  
  public function calculate_result( string $test ) : string ;
      
}

class ParentRequest implements OnlyFor {
   
  public function calculate_result( string $test ) : string
  {
      return (string) $test;
  }

  protected function onlyHere() 
  {
     // 
  }

}

class Child extends ParentRequest implements Only, OnlyFor {
    
    /**
     * Class constructor.
     */
    public function __construct(ParentRequest|Only $data = null)
    {
        
    }
    public function print_result(string $test) : string
    {
        return (string) $test;
    }

} 

```
