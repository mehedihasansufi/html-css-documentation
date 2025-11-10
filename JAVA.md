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




# Multithreading in Java

## Multi Processing
- in operating System at a time i using chrome and vs code that is 
 multiprocess

## Within  a Process Multitasking  that called ***Multithread***
- example in chrome download pdf with server can receive my data that send chorme
- thread are shared process memory
- thread are light weight
- process are heavy weight

## Greating A thread
- by extending thread class
- by implementing runable interface

## Thread Creating 

### By extends Thread

```java
public class thread_class {
    public static void main(String[] args) {

        mythread1 one=new mythread1();
        mythread2 two=new mythread2();
        one.start();
        two.start();

    }
}

class mythread1 extends Thread{
    public void run(){
        while (true){
            System.out.println("Thread one is running");
            System.out.println("I am happy");
        }
    }
}

class mythread2 extends Thread{
    public void main (){
        while (true){
            System.out.println("Thread 2 is running ");
            System.out.println("I am san");
        }
    }
}
```

### Implementing runable interface

```

class mythread1 implements Runnable{
    public void run(){
        System.out.println("I am 1 thread");
    }
}

class mythread2 implements Runnable{
    public void run(){
        System.out.println("i am thread 2");
    }
}


public class thread_class {
    public static void main(String[] args) {

        mythread2 bullet1=new mythread2();
        Thread gun1=new Thread(bullet1);
        mythread1 bullet2=new mythread1();
        Thread gun2=new Thread(bullet2);

        gun1.start();
        gun2.start();

    }
}

```

## Constructor from thread class
