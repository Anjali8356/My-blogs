## JDK, JRE, JVM, and JIT

# How does java code execute?
Java is the most popular, open-source programming language that is used to develop desktop and mobile applications, big data processing, embedded systems, and so on.
All the code that we write in java has an extension as  *.java *. This is human-readable code. Java compiler takes the entire file and converts it into byte code that has an extension as  *.class *. this code is intermediary code that does not run directly on the system. we need a  * Java Virtual Machine *  (JVM)  to run this code. once the JVM runs this code, it gets converted into the Machine code (0's and 1's).

## What are JDK, JRE, JVM, and JIT?

 ### Java Development Kit - JDK

JDK is a software development kit that provides an environment to develop and run the java application. it consists of a compiler *javac*, an interpreter/loader, an archiver, and docs generator-*Javadoc*. java developers can install it on operating systems like Windows, macOS, Solaris, or Linux.

 ### Java Runtime Environment - JRE

It rests in *JDK*. it is also a package that provides an environment to only run the program. you can not create the java programs in JRE .it consists of deployment technologies, user interface toolkits, integration libraries, base libraries, loader class, and JVM. the class loader loads all classes needed to execute the program and JVM sends code to byte code verifier to check.

 ### Java Virtual Machine - JVM

JVM is an engine that converts java bytecode (*.class * file) into machine-readable code. it rests in Java Runtime Enviroment. In many other programming languages, the compiler produces machine code for a specific system. However, the Java compiler produces code for a virtual machine which is called JVM.

 ### Just In Time - JIT

JIT is a part of JVM that acts as a compiler. JVM has a limitation. when we use a function many times in our application, it converts that block of code into machine-specific code again. it repeats the process for every function utilization. this is where we are in Just in time. Just-in-time is a garbage collector that saves the machine code of a function and gives it to the JVM for every repeated utilization of a function. JVM does not have to convert the byte code of a function into machine code again and again. Hence, it improves the performance of Java applications.



Let's understand how does a java source code execute in detail?

 For Instance:

 Let's create a simple program that will print "Hello, World".

```
class HelloWorld {
    public static void main(String[] args) {
        System. out.println("Hello, World!"); 
    }
}
``` 

Note-  Class name will be the same as the file name of the program. Here file name of this program is *HelloWorld.java*.

```
Java source code ---> JDK ---> Bytecode --->  JVM ---> JRE

``` 


**Step 1-** The compiler will take the source file *HelloWorld.java* and check if there is any syntax error or any other compile time error. if no error is found then it will convert it into Byte code (*HelloWorld.class*). this code is platform-independent as you can run it on any other operating system like Linux or macOS. it is only understandable by JVM.

**Step 2-** This is the start of the Run Time Phase. The class loader will load the Byte code into Java Virtual Machine.

**Step 3-** Now Bytecode Verifier verifies the Byte Code and if no issue is found then it will pass the Byte code to an interpreter.

**Step 4-** Now the interpreter inside the JVM converts the Byte Code into Machine Code line by line and passed it to the OS/ Hardware.








