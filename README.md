## 1. Introduction to Java and Development Environment Setup

Java is widely used in modern development due to several key reasons:

- **Platform Independence:**  
  Java code can run on any platform with the Java Virtual Machine (JVM), ensuring cross-platform compatibility.

- **Object-Oriented:**  
  Promotes modular, scalable, and reusable code through object-oriented principles.

- **Rich API and Libraries:**  
  Provides a wide range of built-in libraries for various tasks, speeding up development.  
  **Example:**  
  The `java.util` library provides classes like `ArrayList`, `HashMap`, and `Collections`, which simplify common tasks like storing and manipulating data.
- **Robust and Secure:**  
  Strong memory management, exception handling, and security features ensure reliable and safe applications.

- **Large Ecosystem:**  
  Frameworks like Spring and Hibernate, and tools like Maven and Gradle, support rapid application development.

- **Multithreading Support:**  
  Built-in multithreading capabilities allow concurrent task execution for performance optimization.

- **Enterprise Adoption:**  
  Ideal for building scalable, maintainable enterprise applications because of:
    - **Scalability:** Java's performance, multi-threading, and distributed computing support enable handling large-scale systems.
    - **Maintainability:** Object-oriented design, modularity, and frameworks like Spring promote clean, organized, and easy-to-maintain code.

- **Community Support:**  
  Extensive documentation, tutorials, and an active developer community make learning and development easier.

- **Continuous Evolution:**  
  Regular updates, with new features, ensure Java stays relevant in modern software development.


# 2. JDK vs JRE

### JDK (Java Development Kit)
- **Purpose:**  
  JDK is used for **developing** Java applications. It provides the necessary tools to **write, compile, and debug** Java programs.

- **How it works:**
    - You write Java code in `.java` files.
    - The **JDK** includes the `javac` compiler that **compiles** the `.java` file into a `.class` bytecode file.
    - This compiled `.class` file is a platform-independent bytecode.
    - **JDK** also includes development tools like debuggers, profilers, and the Java API libraries to help build and debug Java applications.

- **Use Case:**  
  Developers use JDK to **write** Java code, **compile** it into bytecode, and run or debug it.

---

### JRE (Java Runtime Environment)
- **Purpose:**  
  JRE is used for **running** Java applications, but it does not provide tools for development.

- **How it works:**
    - Once the `.class` file is created (via JDK), you use **JRE** to **run** the application.
    - The **JRE** contains the **JVM (Java Virtual Machine)**, which is responsible for interpreting and executing the bytecode from the `.class` file.
    - **JRE** also provides core libraries (like `java.lang.*`, `java.util.*`) that are needed to run Java applications.
    - The **JVM** translates the bytecode into machine code that your operating system can execute.

- **Use Case:**  
  Users or systems with JRE installed can run existing Java applications but cannot develop or compile Java code.

---

### Working 
1. You **write** Java code in `.java` files (using any text editor or IDE).
2. **JDK** is used to **compile** the `.java` files into `.class` files (bytecode).
3. The compiled `.class` files are then executed using **JRE**, where the **JVM** runs the bytecode, converting it into machine-specific code for the host system.




# 3. Basic Java Syntax and Core Concepts

## A. Variables, Data Types, and Constants
- **Explanation**: Variables store data values; data types specify the type of data. Constants are immutable variables declared with `final`.

### Primitive Data Types
1. **byte**: 8-bit integer, range -128 to 127.
2. **short**: 16-bit integer, range -32,768 to 32,767.
3. **int**: 32-bit integer, range -2^31 to 2^31-1.
4. **long**: 64-bit integer, range -2^63 to 2^63-1.
5. **float**: 32-bit floating-point number.
6. **double**: 64-bit floating-point number.
7. **char**: Single 16-bit Unicode character.
8. **boolean**: Represents `true` or `false` values.

### Non-Primitive Data Types
1. **Class**: User-defined blueprint for creating objects.
2. **Interface**: Defines methods that a class must implement.
3. **Array**: Collection of elements of the same type.
4. **String**: Sequence of characters.
5. **Enum**: Special data type to define a fixed set of constants.

```java
int age = 25; // Primitive variable
final double PI = 3.14; // Constant (primitive)
String name = "John"; // Non-primitive variable
```

## B. Operators (Arithmetic, Logical, Relational, etc.)
- **Arithmetic Operators**: `+`, `-`, `*`, `/`, `%`
- **Relational Operators**: `==`, `!=`, `>`, `<`, `>=`, `<=`
- **Logical Operators**: `&&`, `||`, `!`

## C. Control Flow (If-else, Switch, Loops)
### If-Else
```java
if (age > 18) {
    System.out.println("Adult");
} else {
    System.out.println("Minor");
}
```

### Switch
```java
switch (day) {
    case 1: System.out.println("Monday"); break;
    default: System.out.println("Other day");
}
```

### Loops
#### For Loop
```java
for (int i = 0; i < 5; i++) {
    System.out.println(i);
}
```

#### While Loop
```java
int i = 0;
while (i < 5) {
    System.out.println(i);
    i++;
}
```

#### Do-While Loop
```java
int i = 0;
do {
    System.out.println(i);
    i++;
} while (i < 5);
```

## D. Functions/Methods and Parameters
- **Explanation**: Methods define reusable blocks of code.
```java
public int add(int a, int b) {
    return a + b;
}
```

## E. Arrays
- **Explanation**: Arrays store multiple values of the same type.
```java
int[] numbers = {1, 2, 3, 4, 5};
System.out.println(numbers[0]); // Access first element
```

## F. Basic Exception Handling (try-catch blocks)
- **Explanation**: Used to handle runtime errors.
```java
try {
    int result = 10 / 0;
} catch (ArithmeticException e) {
    System.out.println("Cannot divide by zero.");
}
```

# 4. Methods in the `Object` Class and Their Usage

The `Object` class provides fundamental methods that every Java class inherits. These methods are essential for comparison, hashing, object cloning, and synchronization. Below is a list of methods in the `Object` class and their descriptions.

### Methods in the `Object` Class:

- **`equals(Object obj)`**  
  Compares this object with another for equality.

- **`hashCode()`**  
  Returns the hash code of the object.

- **`toString()`**  
  Returns a string representation of the object.

- **`getClass()`**  
  Returns the class of the object.

- **`notify()`**  
  Wakes up a single thread waiting on the object.

- **`notifyAll()`**  
  Wakes up all threads waiting on the object.

- **`wait()`**  
  Makes the current thread wait until notified.

- **`wait(long timeout)`**  
  Makes the current thread wait for the specified time.

- **`wait(long timeout, int nanos)`**  
  Waits for the specified time in milliseconds and nanoseconds.

- **`clone()`**  
  Creates a clone of the object (shallow copy).

- **`finalize()`**  
  Used by the garbage collector before the object is destroyed.

These methods provide key functionalities related to object identity, synchronization, cloning, and memory management.



# 5. Object-Oriented Programming (OOP) Basics

---
## a. Classes and Objects
```java
class User {
    String username;
    int userId;

    void login() {
        System.out.println(username + " has logged in.");
    }
}

User user = new User();
user.username = "JohnDoe";
user.userId = 101;
user.login();
```

## b. Constructors
- **Explanation**: Constructors initialize objects and have the same name as the class.
```java
class User {
    String username;

    User(String username) {
        this.username = username;
    }
}

User user = new User("JohnDoe");
```

## c. Instance Variables vs. Class Variables
- **Explanation**: Instance variables belong to an object, while class variables are shared across all instances.
```java
class User {
    String username; // Instance variable
    static String platform = "IAM System"; // Class variable
}

User user1 = new User();
use1.username = "Alice";
System.out.println(User.platform);
```

## d. Methods (Instance Methods, Static Methods)
- **Explanation**: Instance methods require an object to invoke, while static methods belong to the class.
```java
class Authentication {
    void login() { System.out.println("Instance Login Method"); } // Instance Method
    static void logout() { System.out.println("Static Logout Method"); } // Static Method
}
r
Authentication auth = new Authentication();
auth.login();
Authentication.logout();
```

## e. Inheritance
- **Explanation**: Allows a class to inherit properties and methods from another class.
```java
class User {
    void login() { System.out.println("User login."); }
}

class Admin extends User {
    void manageUsers() { System.out.println("Admin managing users."); }
}

Admin admin = new Admin();
admin.login();
admin.manageUsers();
```

## f. Polymorphism (Method Overloading, Method Overriding)
- **Explanation**: Enables methods to perform different tasks based on input or context.
### Method Overriding Example with IAM Concept
```java
class Role {
    void access() { System.out.println("Generic role access."); }
}

class Admin extends Role {
    @Override
    void access() { System.out.println("Admin access to IAM dashboard."); }
}

Role role = new Admin();
role.access();
```

## g. Abstraction (Abstract Classes and Methods)
- **Explanation**: Abstract classes provide a blueprint for other classes, with at least one abstract method (Only method signature)
### Example: Abstract Class with IAM Concept
```java
abstract class IdentityProvider {
    abstract void authenticate();
}

class OktaProvider extends IdentityProvider {
    void authenticate() { System.out.println("Authenticating with Okta"); }
}

IdentityProvider idp = new OktaProvider();
idp.authenticate();
```

## h. Encapsulation (Getters/Setters, Access Modifiers)
- **Explanation**: Encapsulation restricts direct access to fields and provides controlled access through methods.
```java
class User {
    private String password;

    public void setPassword(String password) {
        this.password = password;
    }

    public String getPassword() {
        return password;
    }
}

User user = new User();
user.setPassword("securePass");
System.out.println(user.getPassword());
```

## i. Interfaces and Abstract Classes
- **Explanation**: Interfaces give a list of things a class must do, while abstract classes can do some things and ask the class to do the rest.
- A **default method** in an interface allows you to define a method with a default implementation, which can be overridden by implementing classes if needed and it can not be Abstract.
### Interface Example
```java
interface AuthenticationProvider {
    void authenticate();

    default void displayUser() {
        System.out.println("Displaying the user..");
    }
}

class AzureAD implements AuthenticationProvider {
    public void authenticate() { System.out.println("Authenticating with Azure AD"); }
}

class GoogleAuth implements AuthenticationProvider {
    public void authenticate() {
        System.out.println("Authenticating with Google");
    }

    // Optionally override the default method
    public void displayUser() {
        System.out.println("Another way to display the user...");
    }
}

AuthenticationProvider provider = new AzureAD();
provider.authenticate();

AuthenticationProvider google = new GoogleAuth();
        google.authenticate();
        google.displayUser();
```

## Abstract Classes vs. Interfaces
- Abstract classes can have both abstract and concrete methods, while interfaces only have abstract methods (before Java 8).
- A class can implement multiple interfaces but can extend only one abstract class.

### Example Comparison
#### Abstract Class
```java
abstract class IdentityProvider {
    abstract void authenticate();

    void log() { System.out.println("Logging identity access."); }
}

class KeycloakProvider extends IdentityProvider {
    void authenticate() { System.out.println("Authenticating with Keycloak"); }
}
```

#### Interface
```java
interface SSOProvider {
    void initiateSSO();
}

class GoogleSSO implements SSOProvider {
    public void initiateSSO() { System.out.println("Google SSO initiated."); }
}
```


# 6. Java 8 Features

## 1. Functional Interfaces & Lambda Expressions in Java

### a. Anonymous Classes
Before diving into functional interfaces, it's essential to understand **anonymous classes**. They allow us to create a one-time implementation of an interface by instantiating it directly without creating a separate class.

### Example
```java
Runnable task = new Runnable() {
    @Override
    public void run() {
        System.out.println("Task executed!");
    }
};
new Thread(task).start();
```
## b. **Functional interface** 
- It is an interface with only one abstract method. It can have:
- **One abstract method** (mandatory).
- **Default methods**.
- **Static methods**.
- Methods from the `Object` class (e.g., `toString`, `equals`).

### Common Functional Interfaces
- `Runnable`: Used to execute a task on a separate thread.
- `Callable`: Used to execute a task that returns a result and may throw an exception.
- `Comparator`: Used to define custom sorting logic for objects.

### Different Ways to Implement a Functional Interface

#### 1. Using a Class that Implements the Interface
Create a class, override the abstract method, and use its object.

```java
class AdminValidator implements PermissionValidator {
    @Override
    public boolean validate(String userRole) {
        return "Admin".equals(userRole);
    }
}
PermissionValidator validator = new AdminValidator();
System.out.println(validator.validate("Admin")); // true
```

#### 2. Using an Anonymous Class
Directly instantiate the interface without creating a separate class.

```java
PermissionValidator validator = new PermissionValidator() {
    @Override
    public boolean validate(String userRole) {
        return "Admin".equals(userRole);
    }
};
System.out.println(validator.validate("Admin")); // true
```

#### 3. Using Lambda Expressions
Lambda expressions allow us to write concise, functional-style code.

```java
PermissionValidator isAdmin = role -> "Admin".equals(role);
System.out.println(isAdmin.validate("Admin")); // true
```

### C. Lambda Expressions
- **Definition**: A lambda expression is a concise way to represent a functional interface implementation.
- **Purpose**: Simplifies functional interface usage by removing boilerplate code.
- **Syntax**: `(parameters) -> { body }`

**Example:**
```java
List<String> roles = Arrays.asList("Admin", "User", "Manager");
roles.forEach(role -> System.out.println("Role: " + role));
```

## 3. Types of Functional Interfaces
There are four primary types of functional interfaces based on their purpose:

### a. Consumer<T>
- **Purpose**: Performs an operation on an input (e.g., printing or logging roles in IAM).
- **Abstract Method**: `accept(T t)`
- **IAM Example**: Print user roles to a log.

```java
import java.util.function.Consumer;

Consumer<String> printRole = role -> System.out.println("Role: " + role);
printRole.accept("Admin"); // Output: Role: Admin
```

### b. `Supplier<T>`
- **Purpose**: Supplies a value without any input.
- **Abstract Method**: `get()`
- **Example**:
```java
Supplier<String> defaultRole = () -> "Guest";
System.out.println(defaultRole.get());
```

### c. `Predicate<T>`
- **Purpose**: Tests a condition and returns `true` or `false`.
- **Abstract Method**: `test(T t)`
- **Example**:
```java
Predicate<String> isAdmin = role -> "Admin".equals(role);
System.out.println(isAdmin.test("Admin")); // true
```

### d. `Function<T, R>`
- **Purpose**: Accepts an input and produces an output.
- **Abstract Method**: `apply(T t)`
- **Example**:
```java
Function<String, Integer> roleLength = role -> role.length();
System.out.println(roleLength.apply("Admin")); // 5
```

## c. Streams API

- **Explanation**: We can consider a Stream as a pipeline through which collection elements pass. While elements pass through the pipeline, various operations like `sorted()`, `filter()`, `map()`, `distinct()`, etc., can be performed. Streams are useful for bulk processing and can even handle parallel processing.

### **Steps to Use Streams API**:
1. **Create a stream from a collection.**
2. **Perform intermediate operations** like `sorted()`, `filter()`, `map()`, `distinct()`, etc.
  - These operations transform the stream into another stream, allowing for further operations.
  - These operations are *lazy* in nature, meaning they are only executed when a *terminal operation* is called.
3. **Terminal operations** like `collect()`, `reduce()`, `count()`, etc., trigger the processing of the stream.
  - Once a terminal operation is used, no further operations can be applied to the stream.

---

### **Ways to Create a Stream**

1. **From Collections**
  - A stream can be created from any `Collection` (e.g., List, Set).

   ```java
   List<String> roles = Arrays.asList("Admin", "User", "Manager");
   roles.stream().forEach(System.out::println);
   // Output: Admin, User, Manager
```
2. **From Arrays**
```java
String[] rolesArray = {"Admin", "User", "Manager"};
Arrays.stream(rolesArray).forEach(System.out::println);
// Output: Admin, User, Manager

```

3. **From Static Methods**
```java
Stream<String> roleStream = Stream.of("Admin", "User", "Manager");
roleStream.forEach(System.out::println);
// Output: Admin, User, Manager
```

4. **From Stream Builder**
```java
Stream<String> builderStream = Stream.<String>builder()
        .add("Admin")
        .add("User")
        .add("Manager")
        .build();
builderStream.forEach(System.out::println);
// Output: Admin, User, Manager

```

5. **From Stream Iterate**
```java
Stream<Integer> numbers = Stream.iterate(1, n -> n + 1).limit(5);
numbers.forEach(System.out::println);
// Output: 1, 2, 3, 4, 5


```

### Different Types of Intermediate Operations in Java Streams API

### 1. `filter(Predicate<T> predicate)`
- **Purpose**: Filters elements based on the given predicate.

```java
List<String> users = Arrays.asList("John-Admin", "Alice-User", "Bob-Manager");
users.stream()
     .filter(user -> user.contains("Admin"))
        .forEach(System.out::println);
// Output: John-Admin
```

### 2. map(Function<T, R> mapper)

- **Purpose**: Transforms each element of the stream.

```java
List<String> roles = Arrays.asList("Admin", "User", "Manager");
roles.stream()
     .map(role -> role.toUpperCase())
        .forEach(System.out::println);
// Output: ADMIN, USER, MANAGER
```

### 3. distinct()

- **Purpose**: Removes duplicate elements from the stream.

```java
List<String> users = Arrays.asList("John", "Alice", "Bob", "John");
users.stream()
     .distinct()
     .forEach(System.out::println);
// Output: John, Alice, Bob
```
### 4. sorted()

- **Purpose**: Sorts the elements in the stream.

```java
List<String> roles = Arrays.asList("Manager", "Admin", "User");
roles.stream()
     .sorted()
     .forEach(System.out::println);
// Output: Admin, Manager, User

```

### 5. peek(Consumer<T> action)

- **Purpose**: Performs an action on each element in the stream (used for debugging or viewing elements).

```java
List<String> roles = Arrays.asList("Admin", "User", "Manager");
roles.stream()
     .peek(role -> System.out.println("Role: " + role))
        .collect(Collectors.toList());
// Output: Role: Admin, Role: User, Role: Manager
```

### 6. limit(long maxSize)

- **Purpose**: Limits the number of elements in the stream.

```java
List<String> roles = Arrays.asList("Admin", "User", "Manager", "Guest");
roles.stream()
     .limit(2)
     .forEach(System.out::println);
// Output: Admin, User
```


### 7. skip(long n)

- **Purpose**: Skips the first n elements in the stream.

```java
List<String> roles = Arrays.asList("Admin", "User", "Manager", "Guest");
roles.stream()
     .skip(2)
     .forEach(System.out::println);
// Output: Manager, Guest
```
## Terminal Operations

### 1. `collect(Collector<T, A, R> collector)`
- **Purpose**: Collects the elements of the stream into a collection or other forms.
- **Example**: Collect elements into a list.

```java
List<String> roles = Arrays.asList("Admin", "User", "Manager");
List<String> roleList = roles.stream()
        .collect(Collectors.toList());
System.out.println(roleList);
// Output: [Admin, User, Manager]
```

### 2. reduce(T identity, BinaryOperator<T> accumulator)

- **Purpose**: Performs a reduction on the elements of the stream using an accumulation function and returns an Optional.
- **Example**: Sum of the lengths of all roles.

```java
List<String> roles = Arrays.asList("Admin", "User", "Manager");
int totalLength = roles.stream()
        .reduce(0, (sum, role) -> sum + role.length(), Integer::sum);
System.out.println(totalLength);
// Output: 16
```


### 3. forEach(Consumer<? super T> action)

- **Purpose**: Performs an action for each element of the stream
- **Example**: Print each role.

```java
List<String> roles = Arrays.asList("Admin", "User", "Manager");
roles.stream()
     .forEach(role -> System.out.println(role));
// Output: Admin, User, Manager
```

### 4. count()

- **Purpose**: Returns the number of elements in the stream
- **Example**: Count the number of users with "Admin" role.

```java
List<String> users = Arrays.asList("John-Admin", "Alice-User", "Bob-Admin");
long count = users.stream()
        .filter(user -> user.contains("Admin"))
        .count();
System.out.println(count);
// Output: 2
```



### 5. anyMatch(Predicate<? super T> predicate)
- **Purpose**: Checks if any elements in the stream match the given predicate.
- **Example**: Check if there is any admin user.

```java
List<String> users = Arrays.asList("John-Admin", "Alice-User", "Bob-Manager");
boolean hasAdmin = users.stream()
        .anyMatch(user -> user.contains("Admin"));
System.out.println(hasAdmin);
// Output: true
```


### 6. allMatch(Predicate<? super T> predicate)
- **Purpose**: Checks if all elements in the stream match the given predicate.
- **Example**: Check if all users are admins.

```java
List<String> users = Arrays.asList("John-Admin", "Alice-Admin", "Bob-Admin");
boolean allAdmins = users.stream()
        .allMatch(user -> user.contains("Admin"));
System.out.println(allAdmins);
// Output: true
```


### 7. noneMatch(Predicate<? super T> predicate)
- **Purpose**: Checks if no elements in the stream match the given predicate.
- **Example**: Check if there is no admin user.

```java
List<String> users = Arrays.asList("John-User", "Alice-User", "Bob-Manager");
boolean noAdmin = users.stream()
        .noneMatch(user -> user.contains("Admin"));
System.out.println(noAdmin);
// Output: true
```

### Others: findFirst(), min/max(), toArray()

## Sequence of steam operations 
## Parallel steams
- Helps to perform the steam concurrently, taking advantage of multi core CPU, internally 
  - It uses Task splitter: "splititerator" fucniton to split the data into multiple chunks 
  - Task submission and parallel processing is done using ForkJoinPool

```java
 List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5, 6, 7, 8, 9, 10);
// Using parallel stream to calculate the sum of squares of even numbers
int sumOfSquares = numbers.parallelStream()
        .filter(n -> n % 2 == 0)   // Filter even numbers
        .map(n -> n * n)           // Square each number
        .reduce(0, Integer::sum);  // Sum the squares

        System.out.println("Sum of squares of even numbers: " + sumOfSquares);
```




## d. Default Methods in Interfaces
- **Explanation**: Interfaces can now have method implementations using `default`.
- **Example**: Define a default behavior for user authentication.
```java
interface Authenticator {
    default void authenticate(String user) {
        System.out.println("Authenticating: " + user);
    }
}

class AppAuthenticator implements Authenticator {}

Authenticator auth = new AppAuthenticator();
auth.authenticate("John");
```

## e. Optional Class
- **Usage**: Avoid null pointer exceptions by using `Optional` to handle absent values.
  - Avoiding NullPointerException: Instead of checking if something is null everywhere, you wrap it in an Optional and handle it in a clean, functional way. 
  - Readability: Using Optional makes it explicit when a value might be absent, as opposed to returning null and relying on callers to handle it. 
  - Functional Programming: Many methods, like map, flatMap, and filter, allow for more elegant, chained transformations without worrying about null values.

- Don't Overuse: Optional is useful for return values that can legitimately be absent. It's not meant to replace null everywhere.
```java
Optional<String> user = Optional.ofNullable(null);

// Using orElse to provide a default value
        System.out.println(user.orElse("Default User")); // Default User

        // Using ifPresent to execute action if value is present
        user.ifPresent(u -> System.out.println("User exists: " + u)); // No output

// Using orElseGet for a lazy default value
Optional<String> anotherUser = Optional.ofNullable("Alice");
        System.out.println(anotherUser.orElseGet(() -> "Guest")); // Alice
```

# Java Collections 

## Iterator interface

The `Iterator` interface is a part of the `java.util` package and is used to iterate over a collection of elements, such as lists, sets, and queues. It provides methods to traverse through the elements of a collection and optionally remove elements.

## Methods Exposed by the `Iterator` Interface

The `Iterator` interface exposes three main methods:

1. **`hasNext()`**:
  - Returns `true` if there are more elements to iterate over.
  - Otherwise, it returns `false`.

2. **`next()`**:
  - Returns the next element in the iteration.
  - Throws `NoSuchElementException` if no more elements are available.

3. **`remove()`**:
  - Removes the last element returned by the iterator.
  - Throws `IllegalStateException` if `next()` has not been called, or if `remove()` was already called after the last `next()`.

### Example of Using `Iterator`

```java
import java.util.ArrayList;
import java.util.Iterator;
import java.util.List;

public class IteratorExample {
    public static void main(String[] args) {
        List<String> names = new ArrayList<>();
        names.add("John");
        names.add("Alice");
        names.add("Bob");

        Iterator<String> iterator = names.iterator();

        // Using hasNext() and next()
        while (iterator.hasNext()) {
            System.out.println("Name: " + iterator.next());
        }

        // Using remove() to remove "Alice"
        iterator = names.iterator();  // Reinitialize the iterator to reset
        while (iterator.hasNext()) {
            String name = iterator.next();
            if (name.equals("Alice")) {
                iterator.remove();
            }
        }

        System.out.println("Updated list: " + names);
    }
}

Name: John
Name: Bob
Updated list: [John, Bob]
```

### Example of Using `forEach`

```java
import java.util.List;
import java.util.ArrayList;

public class ForEachExample {
    public static void main(String[] args) {
        List<String> names = new ArrayList<>();
        names.add("John");
        names.add("Alice");
        names.add("Bob");

        // Using forEach to print elements
        names.forEach(name -> System.out.println("Name: " + name));
    }
}

Name: John
Name: Alice
Name: Bob
```

# Java Collection Methods - List Example

In this document, we will explore various methods from the `Collection` interface, using `List` as the collection type. These methods are available in most collection classes like `ArrayList`, `LinkedList`, and others that implement the `Collection` interface.

## Methods in `Collection` Interface

### 1. **`size()`**
- **Purpose**: Returns the number of elements in the collection.

```java

    List<String> names = new ArrayList<>();
    names.add("John");
    names.add("Alice");
    names.add("Bob");
    System.out.println("Size of list: " + names.size());

=   =>     Size of list: 3
```
### 2. isEmpty()
- **Purpose**: Checks if the collection is empty.

```java

    List<String> names = new ArrayList<>();
    System.out.println("Is list empty? " + names.isEmpty());
    names.add("John");
    System.out.println("Is list empty? " + names.isEmpty());
    
    ==>     Is list empty? true
    ==>     Is list empty? false

```

### 3. contains(Object o)
- **Purpose**: Checks if the collection contains the specified element.

```java

    List<String> names = new ArrayList<>();
    names.add("John");
    names.add("Alice");
    System.out.println("Contains Alice? " + names.contains("Alice"));
    
    ==>     Contains Alice? true
```
### 4. toArray()
- **Purpose**: Converts the collection into an array.

```java
    List<String> names = new ArrayList<>();
    names.add("John");
    names.add("Alice");
    Object[] nameArray = names.toArray();
    System.out.println("Array: " + String.join(", ", (CharSequence[]) nameArray));
    
    ==>     Array: John, Alice
```

### 5. add(E e)
- **Purpose**: Converts the collection into an array.

```java
    List<String> names = new ArrayList<>();
    names.add("John"); 
    System.out.println("List: " + names);
    
    ==>     List: [John]
```


### 6. remove(Object o)

- **Purpose**: Removes the specified element from the collection.

```java
    List<String> names = new ArrayList<>();
    names.add("John");
    names.add("Alice");
    names.remove("Alice");
    System.out.println("List after removal: " + names);
    
    ==>     List after removal: [John]
```


### 7. addAll(Collection<? extends E> c)

- **Purpose**: Adds all elements from another collection.

```java
     List<String> names1 = new ArrayList<>();
    names1.add("John");
    List<String> names2 = new ArrayList<>();
    names2.add("Alice");
    names1.addAll(names2);
    System.out.println("Combined list: " + names1);
    
    ==>     Combined list: [John, Alice]
```

### 8. removeAll(Collection<?> c)

- **Purpose**: Adds all elements from another collection.

```java
    List<String> names1 = new ArrayList<>();
    names1.add("John");
    names1.add("Alice");
    List<String> names2 = new ArrayList<>();
    names2.add("Alice");
    names1.removeAll(names2);
    System.out.println("List after removal: " + names1);
    
    ==>    List after removal: [John]
```
### 9. clear()

- **Purpose**: Removes all elements from the collection.

```java
    List<String> names = new ArrayList<>();
    names.add("John");
    names.add("Alice");
    names.clear();
    System.out.println("List after clear: " + names);
    ==>    List after clear: []
```
### 10. equals(Object o)

- **Purpose**: Compares the collection with another collection for equality.
```java
    List<String> names1 = new ArrayList<>();
    names1.add("John");
    names1.add("Alice");
    List<String> names2 = new ArrayList<>();
    names2.add("John");
    names2.add("Alice");
    System.out.println("Are the lists equal? " + names1.equals(names2));
```
### 11. stream()

- **Purpose**: Returns a sequential Stream with the collection's elements.
```java
    List<String> names = new ArrayList<>();
    names.add("John");
    names.add("Alice");
    names.stream().forEach(System.out::println);
    
    ==> John
    ==> Alice
```
### 12. parallelStream()
- **Purpose**: Returns a parallel Stream with the collection's elements.
```java
    List<String> names = new ArrayList<>();
    names.add("John");
    names.add("Alice");
    names.parallelStream().forEach(System.out::println);
    
    ==> John
    ==> Alice
```
### 13. iterator()

- **Purpose**: Returns an iterator for the collection.
```java
    List<String> names = new ArrayList<>();
    names.add("John");
    names.add("Alice");
    Iterator<String> iterator = names.iterator();
    while (iterator.hasNext()) {
        System.out.println(iterator.next());
    }
    
    ==> John
    ==> Alice
```
# Queue Interface Methods

The `Queue` interface in Java represents a collection designed for holding elements prior to processing. Below are the common methods found in the `Queue` interface with brief examples for each.

## Methods in Queue Interface

### 1. `add(E e)`
Adds the specified element to the queue. Throws `IllegalStateException` if the element cannot be added.

```java
Queue<Integer> queue = new LinkedList<>();
queue.add(10);
queue.add(20);
System.out.println(queue); // Output: [10, 20]
```
### 2. offer(E e)
Inserts the specified element into the queue. Returns true if the element was added, false otherwise.
```java
Queue<Integer> queue = new LinkedList<>();
queue.offer(30);
queue.offer(40);
System.out.println(queue); // Output: [30, 40]

```

### 3. poll()
Removes and returns the head of the queue, or null if the queue is empty.

```java
Queue<Integer> queue = new LinkedList<>();
queue.add(50);
queue.add(60);
System.out.println(queue.poll()); // Output: 50
 System.out.println(queue); // Output: [60] 
```

### 4. remove()
Removes and returns the head of the queue. Throws NoSuchElementException if the queue is empty.
```java
Queue<Integer> queue = new LinkedList<>();
queue.add(70);
queue.add(80);
System.out.println(queue.remove()); // Output: 70
 System.out.println(queue); // Output: [80]
```


### 5. peek()
Returns the head of the queue without removing it, or null if the queue is empty.

```java
Queue<Integer> queue = new LinkedList<>();
queue.add(90);
queue.add(100);
System.out.println(queue.peek()); // Output: 90
```


### 6. element()

Returns the head of the queue without removing it. Throws NoSuchElementException if the queue is empty.

```java
Queue<Integer> queue = new LinkedList<>();
queue.add(110);
queue.add(120);
System.out.println(queue.element()); // Output: 110
```

# Priority Queue in Java

A `PriorityQueue` is a type of queue where elements are ordered based on their natural ordering or a custom comparator provided during construction.

## Types of Priority Queues

### 1. Min-Heap (Default Behavior)
A **min-heap** stores elements such that the smallest element is at the root.

```java
PriorityQueue<Integer> minHeap = new PriorityQueue<>();
minHeap.add(30);
minHeap.add(10);
minHeap.add(50);
System.out.println(minHeap.poll()); // Output: 10 (smallest element)
```

### 2. Max-Heap
A **max-heap** stores elements such that the largest element is at the root. It is created using a custom comparator.
```java
PriorityQueue<Integer> maxHeap = new PriorityQueue<>(Collections.reverseOrder());
maxHeap.add(30);
maxHeap.add(10);
maxHeap.add(50);
System.out.println(maxHeap.poll()); // Output: 50 (largest element)
```

# Methods of Deque

This table summarizes the methods of a Deque, categorized by whether they throw an exception or not.

| Method       | Throw Exception (Insert) | Do Not Throw Exception (Insert) | Throw Exception (Remove) | Do Not Throw Exception (Remove) |
|--------------|--------------------------|---------------------------------|--------------------------|---------------------------------|
| **Insert**   | `addFirst`               | `offerFirst`                    | `addLast`                | `offerLast`                     |
| **Remove**   | `removeFirst`            | `pollFirst`                     | `removeLast`             | `pollLast`                      | 
| **Examine**  | `getFirst`                | `peekFirst`                     | `getLast`                |  `peekLast`                     |

```java
Deque<String> deque = new ArrayDeque<>();
        
        // Insert
        deque.addFirst("First");
        deque.addLast("Last");
        
        // Examine
        System.out.println(deque.peekFirst()); // First
        System.out.println(deque.peekLast());  // Last
        
        // Remove
        System.out.println(deque.removeFirst()); // First
        System.out.println(deque.removeLast());  // Last
```

# Methods Specific to the `List` Interface in Java

The `List` interface in Java provides several methods for manipulating ordered collections of elements. Below are the methods that are **specifically defined** in the `List` interface, excluding those inherited from the `Collection` interface.

### 1. **Element Access**
- `E get(int index)`  
  Returns the element at the specified position in the list.

- `E set(int index, E element)`  
  Replaces the element at the specified position in the list with the specified element.

- `int indexOf(Object o)`  
  Returns the index of the first occurrence of the specified element, or -1 if it is not found.

- `int lastIndexOf(Object o)`  
  Returns the index of the last occurrence of the specified element, or -1 if it is not found.

### 2. **List Modifications**
- `void replaceAll(UnaryOperator<E> operator)`  
  Replaces each element of the list with the result of applying the operator to that element.

- `void sort(Comparator<? super E> c)`  
  Sorts the list according to the specified comparator.

### 3. **Sublist Operations**
- `List<E> subList(int fromIndex, int toIndex)`  
  Returns a view of the portion of the list between the specified `fromIndex`, inclusive, and `toIndex`, exclusive.

### 4. **List Iterators**
- `ListIterator<E> listIterator()`  
  Returns a list iterator over the elements in the list, starting at the beginning.

- `ListIterator<E> listIterator(int index)`  
  Returns a list iterator starting at the specified position in the list.

### Example of Using List Methods:

```java
import java.util.*;

public class ListExample {
    public static void main(String[] args) {
        List<String> list = new ArrayList<>();
        
        // Add elements
        list.add("Apple");
        list.add("Banana");
        list.add("Orange");

        // Access elements
        System.out.println("Element at index 1: " + list.get(1)); // Banana
        
        // Replace element
        list.set(1, "Grapes");
        System.out.println("After replace: " + list.get(1)); // Grapes

        // Find index of elements
        System.out.println("Index of 'Grapes': " + list.indexOf("Grapes")); // 1
        System.out.println("Last index of 'Grapes': " + list.lastIndexOf("Grapes")); // 1

        // Using ListIterator
        ListIterator<String> iterator = list.listIterator();
        while (iterator.hasNext()) {
            System.out.println(iterator.next());
        }

        // Replace all elements with a new value
        list.replaceAll(s -> s.toUpperCase());
        System.out.println("After replaceAll: " + list);

        // Sort the list
        list.sort(Comparator.naturalOrder());
        System.out.println("After sort: " + list);

        // Get sublist
        List<String> sublist = list.subList(1, 3);
        System.out.println("Sublist: " + sublist);
    }
}
```

# Methods in the `Map` Interface in Java

The `Map` interface in Java represents a collection of key-value pairs. Below is a list of all methods defined in the `Map` interface, along with their usage.

### 1. **Basic Operations**
- `int size()`  
  Returns the number of key-value pairs in the map.

- `boolean isEmpty()`  
  Returns `true` if the map contains no key-value pairs.

- `boolean containsKey(Object key)`  
  Returns `true` if the map contains the specified key.

- `boolean containsValue(Object value)`  
  Returns `true` if the map contains the specified value.

- `V get(Object key)`  
  Returns the value associated with the specified key, or `null` if the key does not exist.

- `V put(K key, V value)`  
  Associates the specified value with the specified key in the map.

- `V remove(Object key)`  
  Removes the key-value pair for the specified key from the map.

- `void putAll(Map<? extends K, ? extends V> m)`  
  Copies all of the mappings from the specified map to this map.

- `void clear()`  
  Removes all key-value pairs from the map.

### 2. **Special Operations**
- `Set<K> keySet()`  
  Returns a set of all the keys contained in the map.

- `Collection<V> values()`  
  Returns a collection of all the values contained in the map.

- `Set<Map.Entry<K, V>> entrySet()`  
  Returns a set of all the key-value pairs in the map as `Map.Entry` objects.

- `V putIfAbsent(K key, V value)`  
  Adds the specified key-value pair to the map only if the key is not already present.

- `V getOrDefault(Object key, V defaultValue)`  
  Returns the value associated with the specified key, or the default value if the key is not present.

### 3. **Map.Entry Interface**
- `interface Map.Entry<K, V>`  
  Represents a key-value pair in the map.

### Example of Using Map Methods:

```java
import java.util.*;

public class MapExample {
    public static void main(String[] args) {
        Map<String, Integer> map = new HashMap<>();
        
        // Add elements
        map.put("Apple", 1);
        map.put("Banana", 2);
        map.put("Orange", 3);

        // Get the size of the map
        System.out.println("Size: " + map.size()); // 3

        // Check if a key exists
        System.out.println("Contains 'Apple': " + map.containsKey("Apple")); // true

        // Check if a value exists
        System.out.println("Contains value 2: " + map.containsValue(2)); // true

        // Get a value by key
        System.out.println("Value for 'Banana': " + map.get("Banana")); // 2

        // Remove a key-value pair
        map.remove("Apple");

        // Add all entries from another map
        Map<String, Integer> otherMap = new HashMap<>();
        otherMap.put("Grapes", 4);
        map.putAll(otherMap);

        // Get the set of keys
        System.out.println("Keys: " + map.keySet()); // [Banana, Orange, Grapes]

        // Get the collection of values
        System.out.println("Values: " + map.values()); // [2, 3, 4]

        // Get the entry set (key-value pairs)
        System.out.println("Entries: " + map.entrySet()); // [Banana=2, Orange=3, Grapes=4]

        // Put a key-value pair only if absent
        map.putIfAbsent("Orange", 5); // No change, as Orange already exists

        // Get a value with a default if absent
        System.out.println("Value for 'Pineapple': " + map.getOrDefault("Pineapple", 0)); // 0

        // Clear the map
        map.clear();
        System.out.println("Is map empty? " + map.isEmpty()); // true
    }
}
```
