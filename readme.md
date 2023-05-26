## 5. Write a Java program to calculate factorial of n.

```
//factorial.java
//calculate factorial of a number
import java.util.*;
class factorial{
    public void get_fact(){
        Scanner sc =new Scanner(System.in);
        System.out.println("Enter a number");
        int n=sc.nextInt();
        int fact=1;
        for (int i=1; i<=n;i++){
            fact=fact*i;
        }
        System.out.println("Factorial of "+n+ " is "+fact);
        }

    public static void main(String[] args)
    {
      factorial obj=new factorial();
        obj.get_fact();
    }
}
```
## 6. Write a Java program for Fibonacci series.
```
//fibonachii.java
//calculate fibonacii of a number
import java.util.*;
public class fibonachii {
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        System.out.println("Enter a number: ");
        int n=sc.nextInt();
        int a=0;
        int b=1 ;
        System.out.println("Fibonachii series of "+n+" is:");
        if (n==1)
        {
            System.out.println(a);
            System.exit(0);
        }
        System.out.println(a);
        System.out.println(b);
        int c;
        for (int i=3;i<=n;i++)
        {
            c=a+b;
            System.out.println(c);
            a=b;
            b=c;
        }
        
    }
    
}

```
## 7. Write a Java program to find HCF of two Numbers.
```
//hcf.java
//HCF/GCD
import java.util.*;
public class hcf {
public static void main(String[] args) {

    Scanner sc=new Scanner(System.in);
    System.out.println("Enter first number :");
    int a=sc.nextInt();
    System.out.println("Enter second number :");
    int b=sc.nextInt();
    if (a==0 && b==0)
    {
        System.out.println("Can't perform");
        System.exit(0);
    }
    int res=1;
    for (int i=1;i<=b;i++){
        if (a%i==0 && b%i==0)
        {
            res=i;
        }

    }
    System.out.println("HCF of "+a+" and "+b+ " is " +res);
}
}
```
## 8. Write a Java program to find LCM of two Numbers.
```
//hcf.java
import java.util.*;
public class lcm {
public static void main(String[] args) {

    Scanner sc=new Scanner(System.in);
    System.out.println("Enter first number :");
    int a=sc.nextInt();
    System.out.println("Enter second number :");
    int b=sc.nextInt();
    if (a==0 && b==0)
    {
        System.out.println("Can't perform");
        System.exit(0);
    }
    int res=1;
    for (int i=1;i<=b;i++){
        if (a%i==0 && b%i==0)
        {
            res=i;
        }

    }

    int mul=a*b;
    int new_res=mul/res;
    System.out.println("LCM of "+a+" and "+b+ " is " +new_res);
}
}

```
## 9. Write a Java program to count the number of digits of an integer.
```
//count number of digit in a number
//digit.java

import java.util.Scanner;
public class digit {
    
    public static void main(String[] args) {

        int n;
        Scanner sc=new Scanner(System.in);
        System.out.println("Enter a number: ");
        n=sc.nextInt();
        int store=n;
        int count=0;
        while (n!=0){
            n=n/10;
            count++;
        }
        System.out.println("Number of digis in "+store+" is "+count);
        
    }
}

```

## 10. Write a Java program to check whether a number is palindrome or not.

```
//check palindrome or not
//palindrome.java
import java.util.*;
public class palindrome {

    public static void main(String args[])
    {
        Scanner sc=new Scanner(System.in);
        System.out.println("Enter a number");
        int n=sc.nextInt();
        int original=n;
        int rem=0;
        int store=0;
        while(n!=0)
        {
            rem=n%10;
            store=(store *10)+rem;
            n=n/10;
            
        }
        if (store==original)
        {
            System.out.println(original+" is palindrome");
        }
        else{
            System.out.println(original+" is not palindrome");
        }
    }
    
}

```

## 11. Write a Java program to check whether a number is prime or not.

```
//check prime of not 
//prime.java
import java.util.Scanner;

public class prime {
    
    public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter a number: ");
        int n = sc.nextInt();
        boolean flag = true;
        
        for (int i = 2; i <= n-1; i++) {
            if (n % i == 0) {
                flag = false;
                break;
            }
        }
        
        if (flag && n > 1) {
            System.out.println(n + " is a prime number");
        } else {
            System.out.println(n + " is not a prime number");
        }
    }
}

```
## 12. Write a Java program to implement method overloading.
```
//12. Write a Java program to implement method overloading.
//overloading.java
public class overloading {
    public void display(String a)
    {
        System.out.println(a);
    }

    public void display(int a,int b)
    {
        System.out.println(a+b);
    }
    public void display(double a,double b)
    {
        System.out.println(a+b);
    }
     public static void main(String args[])
     {
        overloading obj=new overloading();
        obj.display("hi");
        obj.display(10,20);
        obj.display(10.5,20.5);

     }

}

```

## 13. Write a Java program to implement default constructor or 0-argument Constructor.

```
// Write a Java program to implement default constructor or 0-argument Constructor.
//default.java
class person{
    private int age;
    private String name;
    person()
    {
      this.age=20;
      this.name="Elon";
    }
     void display()
    {
      System.out.println("Name: "+name);
      System.out.println("Age: "+age);
    }
}
public class zero_constructor {
   public static void main(String args[])  
   {
      person obj=new person();
      obj.display();
   }
}

```
## 14. Write a Java program to implement parameterized constructor.
```
//  Write a Java program to implement parameterized constructor.
//para.java
class person{
    private int age;
    private String name;
    person(int a,String b)
    {
      this.age=a;
      this.name=b;
    }
     void display()
    {
      System.out.println("Name: "+name);
      System.out.println("Age: "+age);
    }
}
public class para {
   public static void main(String args[])  
   {
      person obj=new person(30,"Mark");
      obj.display();
   }
}
```
## 15. Write a Java program to implement constructor overloading.
```

//   Write a Java program to implement constructor overloading.
//const_over.java
class person{
    private int age;
    private String name;
    person()
    {
      this.age=20;
      this.name="Elon";
    }
    person(int a,String b)
    {
      this.age=a;
      this.name=b;
    }
     void display()
    {
      System.out.println("Name: "+name);
      System.out.println("Age: "+age);
    }
}
public class const_over {
   public static void main(String args[])   
   {
      person obj=new person();
      obj.display();
      person obj1=new person(30,"Mark");
      obj1.display();
   }
}

```
## 16. Write a Java program to implement static members.

```
// Write a Java program to implement static members.
//check_static.java
class A {
    static int counter = 0; // static variable
    
    A() {
        counter++; // increment counter for each object creation
    }
    
    static void display() {
        System.out.println(counter);
    }
}

public class check_static {
    public static void main(String[] args) {
        A obj1 = new A();
        A obj2 = new A();
        A obj3 = new A();
        A obj4 = new A();
        A obj5 = new A();
        A.display();
    }
}

```
## 17. Write a Java program to implement Single inheritance.
```
//Write a Java program to implement Single inheritance.
//single.java
class A{
    A()
    {
        System.out.println("Constructor of A");
    }
    void display()
    {
        System.out.println("method of A");
    }

}
class B extends A{
    B()
    {
        System.out.println("Constructor of B");
    }
    void display1()
    {
        System.out.println("method of B");
    }
}
public class single {
    public static void main(String args[])
    {
        B obj= new B();
        obj.display();
        obj.display1();
    }
    
}

```
## 18. Write a Java program to implement method overriding in inheritance.

```
//Write a Java program to implement method overriding in inheritance.
//in_over.java
class A{
    A()
    {
        System.out.println("Constructor of A");
    }
    void display()
    {
        System.out.println("method of A");
    }

}
class B extends A{
    B()
    {
        System.out.println("Constructor of B");
    }
    void display()
    {
        System.out.println("method of B");
    }
}
public class in_over {
    public static void main(String args[])
    {
        B obj= new B();
        obj.display();
    }
    
}

```
## 19. Write a Java program to implement multilevel inheritance.
```
// Write a Java program to implement multilevel inheritance.
//multi.java
class A{
    A()
    {
        System.out.println("Constructor of A");
    }
    void display()
    {
        System.out.println("method of A");
    }

}
class B extends A{
    B()
    {
        System.out.println("Constructor of B");
    }
    void display1()
    {
        System.out.println("method of B");
    }
}
class C extends B{
    C()
    {
        System.out.println("Constructor of C");
    }
    void display2()
    {
        System.out.println("method of C");
    }
}


public class multi {
    public static void main(String args[])
    {
        C obj= new C();
        obj.display();
        obj.display1();
        obj.display2();
    }
    
}


```
## 20. Write a Java program to implement interface.
```
//example of interface
//inter.java
interface A{
    void display();
}
class B implements A{
    public void display()
    {
        System.out.println("Method of B");
    }
}

public class inter {
    public static void main(String args[])
    {
         B obj=new B();
         obj.display();
    }
    
}

```
## 21. Write a Java program to implement multiple interface.

```
//java multiple inheritance
//multi_inter.java
interface A{
  void talk();
}
interface B{
    void eat();  
}
interface C{
    void walk();  
}

class D implements A,B,C {
    public void talk(){
        System.out.println("I can talk");
    }
    public void eat(){
        System.out.println("I can eat");
    }
    public void walk(){
        System.out.println("I can walk");
    }
}
public class multi_inter {
    public static void main(String args[])
    {
        D obj=new D();
        obj.talk();
        obj.eat();
        obj.walk();
    }
    
}

```
