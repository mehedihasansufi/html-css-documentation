# Intorducing happiness with java Programming Language

## Static

- Staitc is a keyword in the front of a function that will be cll from main method do not declare any obj

## Variable Convention

- class **(pascal**) -- first charracter capital also like (FirstFunction)
- function (**pascal**) -- first character small like (firstFunction)

## For input

- **Scanner class**

```java
    Scanner input=new Scanner(System.in);
        int age=input.nextInt();
        System.out.println(age);

        input.hasNextInt(); // validity check as user input is int or not

//        for String
        input.next();

//        full of a Sentences
        input.nextLine();
```

## String 
```java
import java.util.Scanner;

public class method {
    public static void main(String[] args) {
        String name=new String("mehedi");
        System.out.println(name);
        
    }
}
```
- String are immutable can't be changed

## String Method
- length ()


## Method 
- Mehtod is like a function that declare in the class

## Method Overloading
- if two method name are same and there parameter also same but return type different **that's method can't be run in java**

```java
import java.util.Scanner;

public class method {

    static void foo (){
        System.out.println("Good Morning bro!");
    }

//    two method name are same but parameter different (that's called method overloading)
    static void foo(int a){
        System.out.println("Good Morning" +a+" times bor!");
    }
    public static void main(String[] args) {

        foo();
        foo(10);
    }
}
```

## Variable argument (VarArgs)

- how many argument send that's not specific 

```java
import java.util.Scanner;

public class method {

 static void sum(int...num) // three dotted
 {
     int totalSum=0;
    for(int value:num){
        totalSum=totalSum+value;
    }
     System.out.println(totalSum);
 }
    public static void main(String[] args) {

     sum(10,20,30);
     sum(10,20,90,70,80);
    }
}
```

## Recursion (now i skip video number 34 codeWithHarry java playlist)



# Intoducing Object Oriented Programming With java
- Inheritance
- Encapsulation
- polymorphism
- Abstraction

## Custom class

- one java file have only one public class