# CSC230

  Scanner sc = new Scanner(System.in);
  String st1 = new String("one two hello world");
  S.o.pln(sc.next()); //print one
  S.o.pln(sc.next()); //print two
  .......
  .......
  
  int x = 200;
  Integer o1 = 5;
  S.o.pln("->" +o1); //print 5
  o1 = x;
  S.o.pln("->" + o1);  //print 200
  
  Integer.MAX_VAULUE
  
  public static void main(String[] args) {
  
  for(int i=0; i < args.length; i++) 
  
  <---------------------------------------------->
  
  
  Chapter 2

  Because when you create a String, it create an object for you. Name James = new Name("James", "Wong"); ///etc
  james.setLast("Wong");
  
  public getLsat() {
  return last;
  }
                                                      refers
  String myStr = james.getLast();    //(String) myStr -------> (obejct string(address)) ------->  "xxxx"(lastname)


  Name jim = james; //same address as james.
  
  (object)jim --------> the address that james points to
  --------------------------------------------------------- // February 5th. 2016
  
                Class     data filed/method
  Public          yes           yes
  default         yes           yes
  protected       no            inheritive
  private         no            yes
  static          no      in dataf and method has only one instance variable(method) exists for all instances (call class varirable)
  final       inheritive  constant in data, inheritive in method
  
  User-modifier: static, final.
  
  Ex:
  public static int counter = 1;
  static public int max(int first, int second) { //statement
  };
  //Then, access this static field/method as:
  
  james.counter //samecounter, get value 1,should avoid this way
  jim.counter++ // same countet, inc by 1, should avoid this way
  Name.counter // same counter, may access by class name, get2
  
  int val = Name.max(10,20); //call max method by class nName.
  
  *to define a static constant data, you need to add "final" constant:*
    public static final float PI = 3.14;
    
    Instance methods can access instance variable and instance methods directly
    Instance methods can caccess class variable and class method directly
    Class methods can access class varables and class mehtods directly
    BUT Classmethods cannot access instance variables or instanc methods directly---they must use an object reference.
    (all these rules above are talking about when in single class)
    
    constructors -- special method -- allocate memory for obejct and initialize data filed. (no return type) has the same name as class name.
    Default constructor is the constructor without parameter. If you do not define any constructors for a class, a default constructor will be provided automatically. If you define a constructor, then a default constructor would not provided.
    
    Accessor (query) methods return value of a data field.
    Mutator methods chage the value of a data field.
    
      Ex.
      public String getLast(); //Accessor method
      public void setLast(String lastName);//Mutator method. 
      
      toString method() : return a string related to object.
      ex. 
      toString() method in Name returns a string first + " " + last
      print(james.toString); // == print(james);
      
      public class A {
      //data//fields.
      in a;
      public int b;
      private int c;
      static public int d;
      static private int e;
      
      //method
      public void f1()
      private void f2()
      void f3() 
      static public f4()
      
      void f5() {list all fileds/methods in Athat can be accessed here} // all can be accessed
      
      static void f6() {list all fields/methods in a that can be accesed here} //only static date/field and method can be access
                                                                               // which are d e , and f4.
      }
      
      class B {      // in same package as A;
      void get () {
      
         ///only private cannot be accessed here
      }
      
      
      publi class C { //in another package 
      
          //only public in A or B can be accessed here
      }
      
      General rules:
      
      Use "this" to avoid confusion, "this" refers to current object
      Ex. Name with filed first and method with parameter first.
      
      //parameter first has the same name as data field first
      
      public void setFirst(String first) {
      this.first = first; //use this.first to refer to data field
      } //end
      
      May use this() to call a constructor from another constructor in the same class. It must be the first statement.
      
      this(); //refer to default constructor in Name
      this("hello", "world"); // refer to 2nd constrctor in Name.
      Class method cannot use "this" keyword as there is no instance for this to refer to
  
  public class NameNew {
    private String first; //first name
    private String last;  //last name
    public int age;
    ...
    public void setLast(String lastName) {
      last = lastName;
    }
    //complete the code later 
    
    ------------------------------------------------------------------------------------------------February 11th.
    
    If this is a referrence data type, have to have referrence.
    
    To return a reference to the current object, use "return this"
    
    
    When a class has a data field that is an instance of another class.
    
    public class Student {
      public Student() {
        private Name student;
        public String id;
      }
      ....
    }
    
    Generic Types: for a class with fields that can be of any class type
    Syntax to define a generic type in a class: public class MyClass <T>
    
    
    
    public class OrderedPair{
    
    .....
    
    
    } //complete later
    
    
    OrderedPair <String> fruit = new OrderedPair <String> ();
    fruit.setPair ("apples", "oranges"); 
    
    Generic type : Primitive types are not allowed! should use wrapper class.***
    
    Restriction on Generics: //later on ilearn.
    
    OrderedPair <int> my Obj = ......; wrong
    OrderedPair <Integer> myObj = ......; correct!
    *******************************************************
    Inheritance ("is a" relationship)
      A general class (or base class, or super class, or parent class) is first defined. Then a derived class (subclass or child class)       is defined.
    
      //Part missing (extend)
      
     *************************************************
      
      
      Abstract mehtod
      
      abstract class GraphicObject {
        int x, y;
        ...
        void moveTo(int newX, int newY) {
        ....
        }
      }
      //Non-abstract class is called concrete class. If there is one method which is abstract, the class has to be abstract.
      
      
      ------------------------------------
      
      int CompareTo(T y);
      //this < y -int
      //this = y 0
      //this > y +int
    
    
    
    
    ---------------------------------------------
    try {
      .
      s1
      s2
      s3
      s4
      .
    }
    Catch (RuntimeError x) {    //a happen here                                       //------     ioexception    b
      .                                              //Exception -----
      s5                                                               //------     runtimeerror   a
      s6
      .
    }
    Catch (Exception x) {       //b happen here
      .
      s7
      s8
      .
    }
    
    finally {
      s9
      s10
    }
    ----------------------------------------------------------------------------------------Feb. 27th.
    
    
    Data Structure starts here:
    
    Modules:
    
    --store data
    --modifying data
    --move and alter data
    
    modulalilty
    --abstraction
    
    
    data abstraction:
    --different way to organize data
    
    Abstract data type: ADT
    
    --type of data
    --operation to support data


    Encapsulation
    
    
    UML: unifying modeling language
    private (-)
    public  (+)
    protect (#)
