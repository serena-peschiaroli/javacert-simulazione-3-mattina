-1 
1 / 45
What will the following class print when compiled and run?
class Holder

{

   int value = 1;

   Holder link;

   public Holder(int val){ this.value = val; }

   public static void main(String[] args)

   {

      final Holder a = new Holder(5);

      Holder b = new Holder(10);

      a.link = b;

      b.link = setIt(a, b);

      System.out.println(a.link.value+" "+b.link.value);

   }

   

   public static Holder setIt(final Holder x, final Holder y)

   {

       x.link = y.link;

       return x;

   }

   

}

The are 1 correct answers

It will not compile because ‘a’ is final.
It will not compile because method setIt() cannot change x.link.
It will print 5, 10.
It will print 10, 10.
- [x] It will throw an exception when run.


__________________________________________________

2 / 45
How many string objects are created in the following code fragment?

Sting a, b, c;

a = new String(“hello”);

b = a;

c = a + b;

The are 1 correct answers

1
2
- [x] 3
4
5


_____________________________________________________
The following method will compile and run without any problems.
public void switchTest(byte x)

{

   switch(x)

   {

      case ‘b’:   // 1

      default :   // 2

      case -2:    // 3

      case 80:    // 4

   }

}

The are 1 correct answers

- [x] True
False


_____________________________________________________
4 / 45
What will the following program print?

class LoopTest

{

   public static void main(String args[])

   {

      int counter = 0;

      outer: for(int i = 0; i < 3; i++)

         middle: for(int j = 0; j < 3; j++)

               inner: for(int k = 0; k < 3; k++)

       {

             if(k-j>0) break middle;

                               counter++;

                          }

    System.out.println(counter);

   }

}

The are 1 correct answers

2
x 3
6
7
9


__________________________________________________
5 / 45
Which of the following statements are true?
The are 2 correct answers
The modulus operator % can only be used with integral operands.
x && can have integral as well as boolean operands.
The arithmetic operators *, / and % have the same level of precedence.
x += can have integral as well as String operands.




___________________________________________________-

6 / 45
What is the result of executing the following fragment of code:

boolean b1 = false;

boolean b2  = false;

if (b2 = b1 != b2)

{

   System.out.println(“true”);

} else

{

   System.out.println(“false”);

}

The are 1 correct answers

Compile time error.
It will print true;
- [x] It will print false;
Runtime error.
It will print nothing.




___________________________________________________

7 / 45
Consider the following code …
class A 

{

    public void doA(int k) throws Exception {  // 0

        for(int i=0; i< 10; i++) {

            if(i == k) throw new Exception("Index of k is "+i); // 1

        }

    }

    public void doB(boolean f) { //2

        if(f) {

            doA(15); //3

        }

        else return;

    }

    public static void main(String[] args) { //4

        A a = new A();

        a.doB(args.length>0); //5

    }

}

Which of the following statements are correct?

The are 1 correct answers

This will compile and run without any errors or exception.
This will compile if ‘throws Exception’ is added at line //2
This will compile if ‘throws Exception’ is added at line //4
- [x] This will compile if ‘throws Exception’ is added at line //2 as well as //4
This will compile if  line marked // 1 is enclosed in a try – catch block.





___________________________________________________

8 / 45
What will the following program print?

public class TestClass

{

  public static void main(String[] args)

  {

     int x = 1;

     int y = 0;

     if( x/y ) System.out.println(“Good”);

     else  System.out.println(“Bad”);

  }

}

The are 1 correct answers

Good
Bad
Exception at runtime saying division by Zero.
- [x] It will not compile.
None of the above.






___________________________________________________
9 / 45
What will the following code print when compiled and run?

The are 1 correct answers


public class OrderTest {

public void initData(String[] arr) {
int ind = 0;
for (String str : arr) {
str.concat(str + " " + ind);
ind++;

}
}

public void printData(String[] arr) {
for (String str : arr) {
System.out.println(str);

}

}

public static void main(String[] args) {
OrderTest ot = new OrderTest();
String[] arr = new String[2];
ot.initData(arr);
ot.printData(arr);

}

}

null 0 null 1
0 1
0 1 (There is a space before 0 and 1)
null null
- [x] It will throw a RuntimeException at run time.




___________________________________________________

10 / 45
Which of the following declarations are valid?
The are 3 correct answers

float f1 = 1.0;
float f = 43e1;
- [x] float f = -1;
- [x] float f = 0x0123;
- [x] float f = 4;



___________________________________________________

11 / 45
Consider the following code:
String s1 = “java”;

String s2= “java”;

String s3 = new String(“java”);

System.out.println(s1 == s2); //1

System.out.println(s1 == s3); //2

System.out.println(s1.equals(s2));//3

System.out.println(s2.equals(s3)); //4

Which lines will print true?

The are 1 correct answers

1, 2, 4
1, 4
3, 4
1, 2, 3, 4
1, 2
1, 2, 3
- [x] 1, 3, 4
___________________________________________________

12 / 45
Consider the following program:

public class TestClass

{

    public int methodA(int a){  return a*2; } //1

    public long methodA(int a){  return a; } //2

    public static void main(String[] args)

    {

        int i = 0;

        i = new TestClass().methodA(2);

        System.out.println( i );

    }

}

The are 1 correct answers

Line 2 correctly overrides the method at line 1.
Line 2 correctly overloads the method at line 1.
There is neither overloading nor overriding happening in the given code but the program will compile fine.
- [x] The program will not compile.
The program will compile and print 4.



___________________________________________________

13 / 45
Given that TestClass is a class, how many objects and reference variables are created by the following code?

TestClass t1, t2, t3, t4;

t1 = t2 = new TestClass();

t3 = new TestClass();

The are 1 correct answers

2 Objects, 3 references.
- [x] 2 Objects, 4 references.
3 Objects, 2 references.
2 Objects, 2 references.
None of the above.





___________________________________________________

14 / 45
What will be the output of the following code snippet?

int a = 1;

int[] ia = new int[10];

int b = ia[a];

int c = b + a;

System.out.println(b = c);

The are 1 correct answers

0
- [x]  1
2
true
false




___________________________________________________

15 / 45
What will be the result of attempting to compile and run the following code?

class TestClass

{

   public static void main(String args[] )

   {

      String str1 = “str1”;

      String str2 = “str2”;

      System.out.println( str1.concat(str2) );

      System.out.println(str1);

   }

}

The are 1 correct answers

The code will fail to compile.
The program will print str1 and str1.
The program will print str1 and str1str2
- [x] The program will print str1str2 and str1
The program will print str1str2 and str1str2



___________________________________________________

16 / 45
What will the following class print when compiled and run?
public class Holder

{

   int value = 1;

   Holder link;

   public Holder(int val){ this.value = val; }

   public static void main(String[] args)

   {

	Holder a = new Holder(5);

	Holder b = new Holder(10);

	a.link = b;

	setIt(a, b);

	System.out.println(a.link.value+", "+b.link.value);

   }

   

   public static void setIt(Holder x, Holder y)

   {

       y.link = x;

   }

   

}
It will print 5, 5.
x It will print 10, 5.
It will print 5, 10.
It will print 10, 10.
None of these.







___________________________________________________


17 / 45
What command should be given to compile and run a java source file named TestClass.java (for standard Oracle JDK)?
The are 1 correct answers

javac TestClass and java TestClass.class
x javac TestClass.java and java TestClass
java TestClass.java and java TestClass
javac TestClass.java and javac TestClass
None of the above.






___________________________________________________

18 / 45
What will the following program print?

public class TestClass

{

  static int someInt = 10;

  public static void changeIt(int a)

  {

    a = 20;

  }

  public static void main(String[] args)

  {

    changeIt(someInt);

    System.out.println(someInt);

  }

}

The are 1 correct answers

x 10
20
It will not compile.
It will throw an exception at runtime.
None of the above.







___________________________________________________

19 / 45
Assuming the declaration of int x = 0;, which of the following code snippets will compile without any errors?
The are 3 correct answers
- [x] while (false) { x=3; }
if (false) { x=3; }
- [x]  do{ x = 3; } while(false);
- [x]  for( int i = 0; i< 0; i++) x = 3;

___________________________________________________

20 / 45
Which of the following statements can be inserted successfully at // 1?

public class InitTest

{

static int si = 10;

int  i;

final boolean bool;

// 1

}

The are 1 correct answers
instance { bool = true; }
InitTest() { si += 10; }
void InitTest(){ si = 5; i = bool ? 1000 : 2000;}
{ i = 1000; }
InitTest() { si += 10; }
InitTest(boolean flag) { bool  = flag; }
- [x] None of the above.









___________________________________________________

21 / 45
Assuming that a valid integer will be passed in the command line as first argument, which statements regarding the following code are correct?

public class TestClass

{

   public static void main(String args[])

   {

      int x = Integer.parseInt(args[0]);

      switch(x)

      {

         case x < 5 : System.out.println(“BIG”); break;

         case x > 5 : System.out.println(“SMALL”);

         default : System.out.println(“CORRECT”); break;

      }

   }

}

The are 1 correct answers

BIG will never be followed be anything else.
SMALL will never follow anything else.
SMALL will always be followed be CORRECT.
- [x] It will not compile.
It’ll throw an exception at runtime.

___________________________________________________


22 / 45
Which of the following are NOT valid operators in Java?
The are 4 correct answers
- [x]  sizeof
- [x] <<< instanceof
    instanceof
 [x]  mod
- [x]  equals



___________________________________________________
23 / 45
Given the code fragment:

    public static void main(String[] args) {

        int[] balances1 = new int[2];

        balances1[0] = 10;

        balances1[1] = 20;

        

        int[] balances2 = balances1;

        balances2[0] = 0;

        

        System.out.print(balances1 == balances2);

    }

What is the result?

Note: You will see real exam questions written in the same format. The question, “what is the result” implies “what is the result of compilation and execution of the given code” assuming that it exists in a valid context such as a class. It does not mean that the code will compile as it is or that it does not have compilation issues.

The are 1 correct answers

- [x] true
false
compilation failure
exception at run time



___________________________________________________

24 / 45
What will the following code snippet print?

   int count = 0, sum = 0;

   do

   {

      if(count % 3 == 0) continue;

      sum+=count;

   }

   while(count++ < 11);

   System.out.println(sum);

The are 1 correct answers

49
- [x]  48
37
36
38



___________________________________________________

25 / 45
Which of the following operators can be used in conjunction with a String object?
The are 3 correct answers

- [x]  +
++
- [x]  +=
- [x] .
*


___________________________________________________

26 / 45
What letters will be printed by this program?

public class ForSwitch

{

    public static void main(String args[])

    {

        char i;

        LOOP: for (i=0;i<5;i++)

        {

            switch(i++)

            {

                case ‘0’: System.out.println(“A”);

                case 1: System.out.println(“B”); break LOOP;

                case 2: System.out.println(“C”); break;

                case 3: System.out.println(“D”); break;

                case 4: System.out.println(“E”);

                case ‘E’ : System.out.println(“F”);

            }

        }

    }

}

The are 2 correct answers

A
B
- [x] C
D
- [x] E
- [x]  F


___________________________________________________

27 / 45
Which of these are keywords in Java?
The are 4 correct answers

- [x] default
null
String
- [x] throws
- [x] long
- [x] strictfp



___________________________________________________

28 / 45
Given the following code:

//1

//2

public class TestClass{

   public static void main(String[] args){

       double d = Math.random();

       System.out.println(d);

   }

}

Which two lines can be inserted at locations marked //1 and //2?

The are 2 correct answers

import java.lang.*;  at //1
import java.util.*;  at //1
- [x] package test;  at //1
package a.b;  at //2
import java.*;  at //2
- [x] import java.lang.*;  at //2


___________________________________________________

29 / 45
What sequence of digits will the following program print?

import java.util.* ;

public class ListTest

{

   public static void main(String args[])

   {

      List s1 = new ArrayList( );

      s1.add(“a”);

      s1.add(“b”);

      s1.add(1, “c”);

      List s2 = new ArrayList(  s1.subList(1, 1) );

      s1.addAll(s2);

      System.out.println(s1);

   }

}

The are 1 correct answers

The sequence a, b, c is printed.
The sequence a, b, c, b is printed.
The sequence a, c, b, c is printed.
- [x] The sequence a, c, b is printed.
None of the above.

___________________________________________________

30 / 45
A try statement must always have a …………. associated with it.
The are 1 correct answers

catch
throws
finally
- [x]  catch, finally or both
throw



___________________________________________________

31 / 45
Given:
The are 1 correct answers

String str = "hello

" + "world";

System.out.println(str.length);

12
13
14
- [x]  Compilation error
Exception at run time

___________________________________________________
32 / 45
Given:
int a = 10, b = 20, c = 30, d = 40;

boolean t = true;

Which of the following statements will print true?

The are 2 correct answers
System.out.println( (a > b) && t);
- [x] System.out.println( (a > b || b < c) && t);
- [x]  System.out.println( (a < d && b < c) || t);
System.out.println( (a > b || t) && (b>c && c>d));




___________________________________________________

33 / 45
Identify correct statements.


The are 2 correct answers

- [x]  1 + Math.random()*9 will return a random number between 1 and 10.
Math.random()*10 will return a random number between 1 and 10.
Math.round(Math.random()*9) will return a random number between 1 and 10.
- [x]  1 + Math.round(Math.random()*9) will return a random number between 1 and 10.
x Math.round(Math.random()*10) will return a random number between 1 and 10.


___________________________________________________
34 / 45
What, if anything, is wrong with the following code?

void test(int x)

{

   switch(x)

   {

      case 1:

      case 2:

      case 0:

      default :

      case 4:

   }

}

The are 1 correct answers

Data Type of ‘x’ is not valid to be used as an expression for the switch clause.
The case label 0 must precede case label 1.
Each case section must be ended by a break keyword.
The default label must be the last label in the switch statement.
- [x]  There is nothing wrong with the code.


___________________________________________________
35 / 45
What letters, and in what order, will be printed when the following program is compiled and run?

public class FinallyTest

{

   public static void main(String args[]) throws Exception

   {

       try

       {

          m1();

          System.out.println(“A”);

       }

       finally

       {

          System.out.println(“B”);

       }

       System.out.println(“C”);

   }

   public static void m1() throws Exception { throw new Exception(); }

}

The are 1 correct answers

It will print C and B, in that order.
It will print A and B, in that order.
- [x] It will print B and then throw an Exception.
It will print A, B and C in that order.


___________________________________________________

36 / 45
Which of these for statements are valid?
The are 1 correct answers

1. for (int i=5; i=0; i -- ) { }

2. int j=5;

for(int i=0, j+=5; i<j ; i++) { j --; }

3. int i, j;

for (j=10; i<j; j -- ) { i += 2; }

4. int i=10;

for ( ; i>0 ; i -- ) { }

5. for (int i=0, j=10; i<j; i++, -- j) {;}

1, 2
3, 4
1, 5
- [x] 4, 5
5


___________________________________________________
37 / 45
Given:
double da[] = new double[3];

Identify correct statements.

The are 1 correct answers
[for(double d : da) System.out.println(d); will print
null
null
null]

[for(int i=1; i<=da.length; i++ ) System.out.println(da[i]); will print
null
null
null]

[for(int i=0; i<=da.length; i++ ) System.out.println(da[i]); will print
null
null
null]
[for(int i=0; i<da.length; i++ ) System.out.println(da[i]); will print
null
null
null]
- [x]   None of the above.







___________________________________________________
38 / 45
Which of the following is true about a Java source file?
The are 3 correct answers

 - [x]  It must have exactly one package statement.
- [x]  It must have zero or more import statements.
- [x]  All classes within the same package as the class are automatically visible to each other without imports.
It can only have zero or one package statement.
All packages from the Java Standard Edition (J2SE) are imported by default.
The source file name has no relation to the classes contained in the file.


___________________________________________________

39 / 45
Which lines contain a valid constructor in the following code?

public class TestClass

{

   public TestClass(int a, int b) { } // 1

   public void TestClass(int a) { }   // 2

   public TestClass(String s); // 3

   private TestClass(String s, int a) { }     //4

   public TestClass(String s1, String s2) { }; //5

}

The are 3 correct answers

- [x] Line // 1
Line // 2
Line // 3
- [x] Line // 4
- [x] Line // 5


___________________________________________________

Which of the following are true about the enhanced for loop?
The are 2 correct answers

It can iterate over an array or a Collection but not an ArrayList.
- [x] Using an enhanced for loop prevents the code from going into an infinite loop.
Using an enhanced for loop on an array may cause infinite loop.
- [x] You cannot find out the number of the current iteration while iterating.



___________________________________________________

41 / 45
Consider the following code for the main() method. What will be the output when the it is executed?
The are 1 correct answers


public static void main(String[] args) throws Exception {

int i =1, j = 10;

do {

if (i++ > -- j) {
continue;

}

}while (i<5);

System.out.println("i="+i+" j="+ j);

}

i=6 j=6
- [x] i=5 j=6
i=5 j=5
i=6 j=5
None of these.


___________________________________________________

Given:
int x = 5;

int y = 9;

int z = 12

boolean b = true;

Which of the following statements will print true?

The are 3 correct answers
x System.out.println( x==y || b );
x System.out.println( ! (x<z) || b );
System.out.println( b == y>z );
System.out.println( b && y>z || z<x );
x System.out.println( !b == y>z );



___________________________________________________
43 / 45
What will the following code print when run?

The are 1 correct answers

public class TestClass {

public static void main(String[] args) throws Exception {

String[] sa = {"a", "b", "c"};

for (String s : sa) {

if ("b".equals(s)) {
continue;

}

System.out.println(s);

if ("b".equals(s)) {
break;

}

System.out.println(s + " again");

}

}

}

- [x]  [a
a again
c
c again]
[a
a again
b]
[a
a again
b
b again]
[c
c again]



___________________________________________________


44 / 45
Consider the following class :

public class Test

{

   public static void main(String[] args)

   {

      if (args[0].equals(“open”))

         if (args[1].equals(“someone”))

            System.out.println(“Hello!”);

      else System.out.println(“Go away “+ args[1]);

    }

}

Which of the following statements are true if the above program is run with the command line :


java Test closed

The are 1 correct answers

x It will throw ArrayIndexOutOfBoundsException at runtime.
It will end without exceptions and will print nothing.
It will print Go away
It will print Go away and then will throw an ArrayIndexOutOfBoundsException.
None of the above.

______________________________________________
45 / 45
Which of the following are features of Java?
The are 2 correct answers

- [x] It allows you to develop distributed applications.
- [x]  It allows you to develop desktop as well as web applications.
It allows development of low level components such as device drivers.
 It is a scripted language.
It is a procedural programming language.