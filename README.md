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
  
  
  public class NameNew {
    private String first; //first name
    private String last;  //last name
    public int age;
    ...
    public void setLast(String lastName) {
      last = lastName;
    }
    
    
