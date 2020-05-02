# Object And Classes Q & A.


1. Describe the relationship between an object and its defining class.
    ```
        Ans: The relationship
        between classes and objects is analogous to that between an apple-pie recipe and apple pies:
        You can make as many apple pies as you want from a single recipe.
    ```

    ```java
        Ex: 
        public class ApplePie {
            String color;
            float weight;
            String[] flavors;
            int noOfSugarSpoons;

           public ApplePie(String color, float weight, String[] flavors, int noOfSpoons) {
               this.color = color;
               this.weight = weight;
               this.flavors = flavors;
               this.noOfSugarSpoons = noOfSpoons;
           }
        }

        public class Main {
            public static void main(String[] args) {
                ApplePie pie1 = new ApplePie("Red", 1.2f, new String[]{"Pineapple"}, 4);
            }
        }
    ```

1. How do you define a class ?

    ```
        Ans: We can define a class by using class keyword.

        Ex: class Car {
                String color;
                public Car() {
                    this.color = "Red";
                }

                public Car(String color) {
                    this.color = color;
                }

                public void setColor(String color) {
                    this.color = color;
                }
        }
    ```

1. How do you declare an object’s reference variable?

    ```
        Ans: By using it class name to define a reference variable.

        Ex:
            Circle c1;
            Square s1;
            Car forGt;
            Car suv;
    ```

1. How do you create an object?

    ```
        Ans: By using new keyword and invoking consturctor.

        
        Ex:
            Car car1 = new Car();
            Car car2 = new Car("Blue", true);
            Square s1 = new Square("Red", true);
            sysout(car2.getColor())
    ```

## Constructors

1. What are the differences between constructors and methods?

    ```
        Ans: i. Constructor will not have return type.
            ii. Constructor will have the same name of the class.
    ```

1. When will a class have a default constructor ?

    ```
        Ans: If user doesnot provide any constructor, java will provide the default constructor to the class.

        Ex: class User {
          
        }
    ```

1. Which operator is used to access a data field or invoke a method from an object?

    ```
        Ans: dot "." operator is used to invoke methods or access data fields.
    ```

1. What is an anonymous object?

    ```
        Ans: Creating a object without assiging it to a reference variable is called anonymous object.

        Ex: new Cricle().getColor()
    ```

1. What is NullPointerException ?

    ```
        Ans: NullPointerException is a common runtime error. It occurs when you invoke
            a method on a reference variable with a null value.
        
        Ex: Cricle c1 = null;
            c1.getColor();
    ```

1. Is an array an object or a primitive type value?

    ```
        Ans: An array is a object.
    ```

1. Can an array contain elements of an object type?

    ```
        Ans: Yes
    ```

1. Describe the default value for the elements of an array ?

    ```
        Ans: Default values are the values which are creating while initializing an array.
    ```

1. What is wrong with each of the following programs?

    ```java
        1. public class ShowErrors {
        2.    public static void main(String[] args) {
        3.       ShowErrors t = new ShowErrors(5);
        4.  }
        5. }

        Ans: There is a error in line number 3, because there is no constructor in ShowErrors class, which is taking int as a argument.
    ```

    ```java
        1. public class ShowErrors {
        2.    public static void main(String[] args) {
        3.       ShowErrors t = new ShowErrors();
        4.       t.x();
        5.  }
        6. }

        Ans: Line 4 is worng, as there is no method x defined in class ShowErrors.
    ```

    ```java
            1. public class ShowErrors {
            2. public void method1() {
            3. Circle c;
            4. System.out.println("What is radius "
            5. + c.getRadius());
            6. c = new Circle();
            7. }
            8. }

            Ans: Line 4 is worng, The local variable c may not have been initialized.
    ```

    ```java
        1. public class ShowErrors {
        2.      public staic void main(String[] args) {
        3.         C c = new C(5.0);
        4.         System.out.println(c.value);
        5.      }
        6.  }
        7.  class C {
        8.    int value = 2;
        9. }

        Ans: Line 3 is wrong, because there is no constructor in class C which takes dobule/float as argument.
    ```

    1. What is the output of following  code?

        ```java
            public class A {
                boolean x;

                public static void main(String[] args) {
                    A a = new A();
                    System.out.println(a.x);
                }
            }

            Ans: false
        ```

    1. How do you create a Date for the current time? How do you display the current time?

        ```
        Ans: 
            Date d = new Date(); // Creating object for current time
            System.out.println(d.toString()); // Printing current date and time
        ```

    1. How do you create a Point2D? Suppose p1 and p2 are two instances of Point2D?
        How do you obtain the distance between the two points?

        ```
        Ans: Point2D p1 = new Point2D(2, 2); // Creating Point2D p1
		Point2D p2 = new Point2D(5,  5); // Creating Point2D p2
		System.out.println(p1.distance(p2)); // claculating distance between p1 and p2.
        ```
    
    1.  Which packages contain the classes Date, Random, Point2D, System, and Math?

        ```
        Ans: Date belongs to java.util.
            Randome belongs to java.util.
            Point2D belongs to javafx.geometry.
            System belongs to java.lang
            Math belongs to java.lang
        ```
    
1. What is an accessor method? What is a mutator method? What are the naming conventions for accessor methods and mutator methods?

    ```
     Ans: Accessor method is used to get the values of data fields.
     Mutator methods is used to change the values of data fields.
     Accessot methods starts with get.
     Mutator methods starts with set.
    ```

1. What are the benefits of data field encapsulation?

```
Ans:  Protects data and makes the class easy to maintain.
We can achive data field encapsulation by using private access modifier which will prevent prevent direct modifications of data fields.
```