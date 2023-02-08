# Why Java 8?

# What is Lambda Expression?
1. Lambda is equivalent to a function (method) without a name.
2. Lambdas are also referred as Anonymous functions.
3. Lambdas are not tied to any class like a regular method.
4. Lambda can also be assigned to variable and passed around.
5. Lambda is mainly used to implement Functional Interfaces(SAM - Single Abstract Method)
6. Lambda expression consists of
   a. Method parameters
   b. Method Body
   c. Return Type

# What is functional interface?
1. If an interface has just one abstract method then those interfaces are categorized as functional interfaces.
2. All those Single Abstract Method interfaces are annotated with @FunctionalInterface annotation.
3. Some existing functional interfaces prior to Java 8 are Runnable and Comparator.
4. Functional interface can have any number of default, static methods but can contain only one abstract method.
   
   @FunctionalInterface
   public interface Comparator<T> {
      int compare(T 01, T 02);
   }
   @FunctionalInterface 
   public interface Runnable {
      public abstract void run();
   }
5. By default, methods defined in an interface are abstract and no need to mention abstract keyword to define it.

# Static and default methods
1. In Java 8, static and default methods are introduced in interfaces.
2. These methods can have their implementation in interface itself, whereas abstract methods can have method 
definition in interface.

   interface MyFunctionalInterface {
      public void execute(); 
      public default void print (String text) { 
         System.out.println(text); 
      } 
      public static void print(String text, PrintWriter writer) {
         writer.write(text); 
      }
   }

# Lambda vs Method
Lambda expression in Java has these main parts:
1. No Name - As Lambda is an anonymous function so no need to have a name
2. Parameter list
3. Body - This is the main part of the function No
4. Return Type - You don't need to mention the return type in the lambda expression. The Java 8+ compiler 
infers the return type by checking the code

# Lambda Expression Syntax
            ()             ->             { }
Lambda Input Parameters  Arrow  (Denoting Lambda) Body Lambda