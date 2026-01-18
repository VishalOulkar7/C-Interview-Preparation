# C-Interview-Preparation


  C# Interview Quetions 
----------------------
1.Have you worked on Any Design Pattern in C# (***)
2.Explain Design Principles in C# (***)
3.How to Authenticate Web API (**)
4.Difference Between Interface and Abstract Class ? (***)
5.When to use Interface and when to Use Abstract Class (**)
6.Exception Handling in C# (**)
7.DIfferent Between Data Abstraction and Encapsulation (*)
8.Explain Private Constructor? Which scenario we use private constructor (***)
9.Different between Convert.ToString() and .ToString() (*)
10.Serialization in C# (**)
11.Generics in c# (***)
12.Events and Delegates in C# (**)
13.COllections in c#(*)
14.Different Between Array and ArrayList in c# (**)
15.String is value type or reference type? (*)
16.What is Reflection in C# (**)
17.Different Between Ref and Out in C# (****)
18.Different Between IEnumarable and IQuarable in c#(****)
19.Garbage Collections in C# (***)
20.Exaplain Method Overloading and Method Overriding(Polymorphisom) in C# (**)
21.Explain Singletop Design Pattern(***)
22.When to Use Static CLass(**)
23.Can we create Static Constructor (**)
24.Types of Constructor (*)
25.Exaplin Inheritance in C# (*)
26.Different Between Var and Dynamic in C# (***)
27.Explain Virtual and Override Key word in c#(*)
28.Explain Threading in C# (**)
29.Exalin async and Await in c# (**)
30.How to do to Bulk Insertion to SQL From C# (*)
31.what is Transactions in c# (*)
32.what is Using in C# (***)
33.Different Between Constant and Read-Only in c# (***)
34.What is Sealed Class in C# (**)
35.Can a private virtual method can be overridden? (*)
36.What’s the difference between the System.Array.CopyTo() and System.Array.Clone() ? (*)
37.What is the difference between Finalize() and Dispose() methods? (**)
38.What is an object pool in .NET? (*)
39.What are Custom Exceptions? (*)
40.What are delegates? (**)
41.How to use nullable types in .Net? (*)
42.What is difference between "is" and "as" operators in c#? (*)
43.What is difference between the "throw" and "throw ex" in .NET? (*)
44.Is C# code is managed or unmanaged code?(*)
45.What is the difference between continue and break statements in C#? (*)
46.What is Boxing and Unboxing? (*)
47.What is namespace in C#? (*)
48.Why to use finally block in C#?
49.if i writte System.Exit in Try block will the execution will go to Finally Block? (**)
50.Can you return multiple values from a function in C#? Provide some examples (**)
51.Explain Anonymous type in C# (**)
52.Explain the difference between Task and Thread in .NET(**)
53.What is the yield keyword used for in C#? (**)
54.Why to use lock statement in C#? (*)

C# Interview Questions & Answers

1. Have you worked on Any Design Pattern in C#? (***)
Answer: Yes, I have worked with several design patterns, such as:
* Singleton Pattern (Ensures only one instance of a class is created.)
* Factory Pattern (Used to create objects without specifying the exact class.)
* Repository Pattern (Used in data access layers to manage database operations.)
* Observer Pattern (Useful for event handling in applications.)
*  Dependency Injection (DI): Providing dependencies to a class from an external source rather than creating them within the class.
* Adapter: Allows interfaces of incompatible classes to work together by wrapping its own interface around that of an already existing class.
 
2. Explain Design Principles in C#? (***)
Answer: The five SOLID principles are:
* S – Single Responsibility Principle (SRP): A class should have only one reason to change.
* O – Open/Closed Principle (OCP): Classes should be open for extension but closed for modification.
* L – Liskov Substitution Principle (LSP): Subtypes must be replaceable with their base types without altering functionality.
* I – Interface Segregation Principle (ISP): Clients should not be forced to depend on interfaces they do not use.
* D – Dependency Inversion Principle (DIP): Depend on abstractions, not concrete implementations.

3. How to Authenticate Web API? (**)
Answer: Authentication in Web API can be done using:
* Token-based Authentication (JWT - JSON Web Token)
* OAuth 2.0 (Used for secure authorization)
* Basic Authentication (Username & password in headers)
* API Keys (A key-based authentication approach)
* Windows Authentication (For intranet applications)

4. Difference Between Interface and Abstract Class? (***)
Feature	Interface	Abstract Class
Methods	Only declarations (no implementation)	Can have implemented methods
Fields	Cannot have fields	Can have fields
Constructors	No constructor	Can have a constructor
Multiple Inheritance	Supports multiple interface implementation	Cannot inherit multiple abstract classes
Use Case	When different classes need to follow the same contract	When classes share a common base functionality
5. When to use Interface and when to use Abstract Class? (**)
* Use an Interface when you want to define a contract that multiple classes should follow.
* Use an Abstract Class when you want to provide some shared implementation while still allowing customization in derived classes.

6. Exception Handling in C#? (**)
Answer: Exception handling ensures code runs smoothly even when unexpected errors occur. It is done using:
try {
   // Code that may cause an exception
} catch (Exception ex) {
   // Handle exception
} finally {
   // Optional block that executes regardless of exception
}
Common exceptions:
* NullReferenceException (Accessing null objects)
* IndexOutOfRangeException (Invalid array index)
* DivideByZeroException (Dividing by zero)

7. Difference Between Data Abstraction and Encapsulation? (*)
* Abstraction hides implementation details and only shows essential features (e.g., interfaces, abstract classes).
* Encapsulation restricts direct access to data using access modifiers (private, public, protected).
Example:
public abstract class Vehicle { 
   public abstract void Start(); // Abstraction
}

public class Car : Vehicle {
   private int speed; // Encapsulation
   public override void Start() { }
}

8. Explain Private Constructor? When is it used? (***)
Answer: A private constructor prevents object instantiation from outside the class.
* Used in Singleton Pattern to ensure a single instance.
* Used in Utility Classes to prevent object creation.
Example:
public class Singleton {
   private static Singleton instance;
   private Singleton() { } // Private Constructor
   public static Singleton GetInstance() {
      if (instance == null) instance = new Singleton();
      return instance;
   }
}

9. Difference Between Convert.ToString() and .ToString()? (*)
Method	Behavior
.ToString()	Throws an exception if the object is null
Convert.ToString()	Returns an empty string if the object is null
Example:
object obj = null;
Console.WriteLine(Convert.ToString(obj)); // ""
Console.WriteLine(obj.ToString()); // Throws NullReferenceException

10. Serialization in C#? (**)
Answer: Serialization converts objects into a format (JSON, XML, Binary) for storage or transmission.
* JSON Serialization: JsonConvert.SerializeObject(obj);
* Binary Serialization: BinaryFormatter.Serialize(stream, obj);
* XML Serialization: XmlSerializer.Serialize(stream, obj);
Example:
using System.Text.Json;
Person p = new Person { Name = "John", Age = 30 };
string json = JsonSerializer.Serialize(p);

11. Generics in C#? (***)
Answer: Generics allow code reuse by enabling type safety.
public class GenericClass<T> {
 public T Value { get; set; }
}
GenericClass<int> obj = new GenericClass<int>();
Benefits:
* Type safety
* Code reusability
* Performance improvement

12. Events and Delegates in C#? (**)
Answer:
* Delegate is a type that references a method.
* Event is a notification mechanism that allows a class to notify subscribers when something happens.
Example:
public delegate void MyDelegate(string message);
public class EventExample {
   public event MyDelegate MyEvent;
   public void TriggerEvent() {
      if (MyEvent != null) MyEvent("Event Triggered");
   }
}

13. Collections in C#? (*)
Answer: Collections in C# are used to store and manipulate groups of objects. Common types:
* List – A resizable array
* Dictionary<TKey, TValue> – A key-value pair collection
* Queue – FIFO (First In, First Out)
* Stack – LIFO (Last In, First Out)
* HashSet – A collection of unique elements
Example:
List<int> numbers = new List<int> { 1, 2, 3, 4, 5 };
numbers.Add(6);

14. Difference Between Array and ArrayList in C#? (⭐⭐)
Feature	Array	ArrayList
Type Safety	Strongly typed	Not type-safe (stores object)
Performance	Faster (no boxing/unboxing)	Slower (boxing/unboxing for value types)
Size	Fixed size	Dynamically grows
Namespace	System	System.Collections
Generic Equivalent	T[]	List<T> (Recommended)
Example:
// Array (Fixed size)
int[] numbers = new int[3] { 1, 2, 3 };

// ArrayList (Dynamic size, but not type-safe)
ArrayList list = new ArrayList();
list.Add(1);   // Boxing (int -> object)
list.Add("Hello"); // No type safety
🔹 Best Practice: Use List<T> instead of ArrayList for better performance.

15. Is string a Value Type or Reference Type? (⭐)
Answer: string is a reference type, but it behaves like a value type because it is immutable.
string s1 = "Hello";
string s2 = s1;
s1 = "World";

Console.WriteLine(s2); // Output: Hello (not affected by s1 change)
🔹 Explanation: Even though s1 is changed, s2 still holds "Hello" because strings are immutable.

16. What is Reflection in C#? (⭐⭐)
Reflection is a feature that allows introspection of assemblies, types, and members at runtime.
Example:
using System;
using System.Reflection;

Type type = typeof(String);
MethodInfo[] methods = type.GetMethods();

foreach (MethodInfo method in methods)
    Console.WriteLine(method.Name);
🔹 Use Cases: ✅ Inspect assemblies, classes, and methods dynamically ✅ Create objects at runtime (Activator.CreateInstance) ✅ Used in Dependency Injection, Unit Testing, and Serialization

17. Difference Between ref and out in C#? (⭐⭐⭐⭐)
Feature	ref	out
Initialization	Must be initialized before passing	Does not require initialization
Purpose	Pass variable by reference	Return multiple values
Usage	Modify an existing value	Assign a new value
Example:
void Example(ref int a, out int b)
{
    a += 10; // Must be initialized before passing
    b = 20;  // Must be assigned before returning
}

int x = 5, y;
Example(ref x, out y);
Console.WriteLine($"{x}, {y}"); // Output: 15, 20

18. Difference Between IEnumerable and IQueryable? (⭐⭐⭐⭐)
Feature	IEnumerable	IQueryable
Namespace	System.Collections	System.Linq
Execution	In-memory (deferred execution)	Database-side execution
Performance	Slower for large data	Faster for large data (optimized queries)
Use Case	Small collections	LINQ-to-SQL queries
🔹 Example:
IEnumerable<int> nums = myDbContext.Numbers.ToList();  // Loads everything into memory
IQueryable<int> numsQuery = myDbContext.Numbers;       // Executes SQL query efficiently

19. Garbage Collection in C#? (⭐⭐⭐)
🔹 Garbage Collector (GC) automatically frees memory by removing unused objects. 🔹 C# has 3 generations of GC: ✅ Gen 0: Short-lived objects (fast cleanup) ✅ Gen 1: Medium-lived objects ✅ Gen 2: Long-lived objects
GC.Collect();  // Manually trigger garbage collection (not recommended)

20. Explain Method Overloading vs. Method Overriding? (Polymorphism) (⭐⭐)
Feature	Method Overloading	Method Overriding
Purpose	Multiple methods with same name but different parameters	Replace base class method in derived class
Signature	Different parameters	Same parameters
Inheritance	Not required	Requires inheritance
Keyword	No special keyword	Uses override keyword
// Method Overloading
class Example {
    void Print(int x) { }
    void Print(string y) { }
}

// Method Overriding
class Base {
    public virtual void Show() => Console.WriteLine("Base Show");
}
class Derived : Base {
    public override void Show() => Console.WriteLine("Derived Show");
}

21. Explain Singleton Design Pattern? (⭐⭐⭐)
A Singleton ensures only one instance of a class exists.
public sealed class Singleton
{
    private static readonly Singleton _instance = new Singleton();
    private Singleton() { }
    public static Singleton Instance => _instance;
}
🔹 Use Cases: Database connections, logging, configuration managers

22. When to Use a static Class? (⭐⭐)
🔹 Use static classes when you need utility/helper methods and don't require object instantiation.
public static class MathHelper {
    public static int Square(int x) => x * x;
}
✅ Use Cases: Math, Console, DateTime

23. Can We Create a Static Constructor? (⭐⭐)
Yes, a static constructor is called only once per type.
class Example {
    static Example() { Console.WriteLine("Static Constructor"); }
}
🔹 Use Case: Initialize static fields before use.

24. Types of Constructors in C#? (⭐)
Constructor	Description
Default Constructor	No parameters
Parameterized Constructor	Takes parameters
Copy Constructor	Copies values from another object
Static Constructor	Initializes static members
public class Example {
    public Example() { }        // Default
    public Example(int x) { }   // Parameterized
    public Example(Example e) { } // Copy
}

25. Explain Inheritance in C#? (⭐)
Inheritance allows code reusability by deriving classes from a base class.
class Animal { public void Eat() => Console.WriteLine("Eating"); }
class Dog : Animal { public void Bark() => Console.WriteLine("Barking"); }
✅ Use Case: Reuse logic from the base class.

26. Difference Between var and dynamic in C#? (⭐⭐⭐)
Feature	var	dynamic
Type Resolution	Compile-time	Runtime
Performance	Fast	Slow (runtime type checking)
IntelliSense	Available	Not available
var a = 10;       // Compile-time type checked
dynamic b = 10;   // Runtime type checked
b = "Hello";      // No error at compile time
✅ Use var for known types and dynamic when you don't know the type in advance.

Commonly Asked Tricky C# Interview Questions (10+ Years Experience)
Here are the next set of tricky C# interview questions along with their explanations and examples.

27. Explain virtual and override Keywords in C#? (⭐)
🔹 The virtual keyword declares a method that can be overridden in derived classes. 🔹 The override keyword is used in a derived class to replace the base class method.
Example:
class Base {
    public virtual void Show() => Console.WriteLine("Base class method");
}

class Derived : Base {
    public override void Show() => Console.WriteLine("Derived class method");
}

Base obj = new Derived();
obj.Show(); // Output: Derived class method
✅ Use Case: Polymorphism, when you want a base method to be overridden in child classes.

28. Explain Threading in C#? (⭐⭐)
🔹 Threading allows parallel execution of tasks, improving performance. 🔹 The Thread class is used to create and manage threads.
Example:
using System;
using System.Threading;

class Program {
    static void PrintNumbers() {
        for (int i = 1; i <= 5; i++) {
            Console.WriteLine(i);
            Thread.Sleep(500);
        }
    }

    static void Main() {
        Thread t = new Thread(PrintNumbers);
        t.Start();
    }
}
✅ Use Case: Background tasks, parallel execution, improving performance.

29. Explain async and await in C#? (⭐⭐)
🔹 The async keyword marks a method as asynchronous. 🔹 The await keyword pauses execution until the async method completes.
Example:
using System;
using System.Threading.Tasks;

class Program {
    static async Task PrintMessage() {
        await Task.Delay(2000);
        Console.WriteLine("Hello after 2 seconds");
    }

    static async Task Main() {
        Console.WriteLine("Start");
        await PrintMessage();
        Console.WriteLine("End");
    }
}
✅ Use Case: Non-blocking I/O, API calls, database queries.

30. How to Perform Bulk Insert in SQL from C#? (⭐)
🔹 Use SqlBulkCopy for fast bulk insertion.
using System.Data;
using System.Data.SqlClient;

class Program {
    static void Main() {
        using (SqlConnection conn = new SqlConnection("your_connection_string")) {
            conn.Open();

            DataTable dt = new DataTable();
            dt.Columns.Add("Name");
            dt.Rows.Add("Vishal");

            using (SqlBulkCopy bulkCopy = new SqlBulkCopy(conn)) {
                bulkCopy.DestinationTableName = "Employees";
                bulkCopy.WriteToServer(dt);
            }
        }
    }
}
✅ Use Case: Inserting large amounts of data efficiently.

31. What is a Transaction in C#? (⭐)
🔹 A transaction ensures that a series of database operations execute completely or not at all.
Example using TransactionScope:
using (TransactionScope scope = new TransactionScope()) {
    // Perform DB operations here
    scope.Complete(); // Commit transaction
}
✅ Use Case: Bank transactions, critical operations.

32. What is using in C#? (⭐⭐⭐)
🔹 using ensures that resources are disposed automatically.
Example:
using (StreamWriter writer = new StreamWriter("file.txt")) {
    writer.WriteLine("Hello, Vishal!");
} // File is automatically closed here
✅ Use Case: File handling, database connections.

33. Difference Between const and readonly in C#? (⭐⭐⭐)
Feature	const	readonly
Value Assignment	Must be assigned at compile time	Can be assigned in constructor
Modifiability	Cannot change after declaration	Can be assigned once in the constructor
Storage	Stored in assembly metadata	Stored in heap memory
Example:
const double Pi = 3.14; // Compile-time constant
readonly int id; // Assigned in constructor

public Program(int val) { id = val; } // Allowed for readonly

34. What is a sealed Class in C#? (⭐⭐)
🔹 sealed prevents inheritance.
Example:
sealed class A { } // Cannot be inherited
class B : A { } // Error
✅ Use Case: Security, preventing unwanted modifications.

35. Can a Private Virtual Method Be Overridden? (⭐)
No, a private method cannot be overridden because it is not accessible in derived classes.

36. Difference Between Array.CopyTo() and Array.Clone()? (⭐)
Feature	CopyTo()	Clone()
Copies Data	Copies elements to another existing array	Creates a new array
Deep or Shallow Copy	Shallow copy	Shallow copy
Example:
int[] arr = {1, 2, 3};
int[] arrClone = (int[])arr.Clone(); // New array

37. Difference Between Finalize() and Dispose()? (⭐⭐)
Feature	Finalize()	Dispose()
Call Type	Called by GC	Called explicitly
Override	Yes, in destructors	Yes, via IDisposable
Example:
class MyClass : IDisposable {
    ~MyClass() { Console.WriteLine("Finalize called"); }
    public void Dispose() { GC.SuppressFinalize(this); }
}

38. What is an Object Pool in .NET? (⭐)
🔹 Object pooling reuses objects instead of creating new instances.
✅ Use Case: Improves performance in high-memory applications.

39. What are Custom Exceptions in C#? (⭐)
🔹 Custom exceptions allow better error handling.
Example:
class MyException : Exception {
    public MyException(string message) : base(message) { }
}

40. What are Delegates in C#? (⭐⭐)
🔹 A delegate is a type that holds method references.
Example:
public delegate void MyDelegate(string message);

class Program {
    static void PrintMessage(string msg) => Console.WriteLine(msg);

    static void Main() {
        MyDelegate del = PrintMessage;
        del("Hello, Vishal!");
    }
}
✅ Use Case: Callbacks, event handling.


🚀 More Tricky C# Interview Questions (10+ Years Experience)
Here are the next set of tricky C# interview questions along with their explanations and examples.

41. How to Use Nullable Types in .NET? (⭐)
🔹 Nullable types allow value types (int, double, bool, etc.) to hold null.
Example:
int? num = null; // Nullable integer
num = 10; // Assign a value

if (num.HasValue)
    Console.WriteLine(num.Value); // Output: 10
✅ Use Case: Database operations, optional values.

42. Difference Between is and as Operators in C#? (⭐)
🔹 is checks type compatibility and returns true/false. 🔹 as performs safe type casting, returning null if casting fails.
Example:
object obj = "Hello";
bool check = obj is string; // true

string str = obj as string; // "Hello"
✅ Use Case: Type checking, safe casting.

43. Difference Between throw and throw ex in .NET? (⭐)
Feature	throw	throw ex
Stack Trace	Preserves original stack trace	Resets stack trace
Use Case	Re-throws original exception	Modifies exception
Example:
try {
    throw new Exception("Error!");
} catch (Exception ex) {
    throw; // Preserves stack trace
    // throw ex; // Resets stack trace (not recommended)
}

44. Is C# Managed or Unmanaged Code? (⭐)
🔹 C# is managed code because it runs under the .NET runtime (CLR). 🔹 Unmanaged code refers to direct memory handling (C, C++).

45. Difference Between continue and break in C#? (⭐)
Feature	continue	break
Behavior	Skips current iteration and continues	Exits loop immediately
Example:
for (int i = 1; i <= 5; i++) {
    if (i == 3) continue; // Skip iteration
    Console.WriteLine(i);
}
// Output: 1, 2, 4, 5

46. What is Boxing and Unboxing? (⭐)
🔹 Boxing: Converts a value type to an object. 🔹 Unboxing: Extracts a value type from an object.
Example:
int num = 10;
object obj = num; // Boxing
int newNum = (int)obj; // Unboxing
✅ Use Case: Performance optimization, memory management.

47. What is a Namespace in C#? (⭐)
🔹 Namespace organizes code into logical groups to avoid naming conflicts.
Example:
namespace MyNamespace {
    class MyClass { }
}
✅ Use Case: Large projects, modular design.

48. Why Use the finally Block in C#? (⭐)
🔹 Ensures code execution even if an exception occurs. 🔹 Typically used for clean-up operations.
Example:
try {
    Console.WriteLine("Try Block");
} finally {
    Console.WriteLine("Finally Block Always Runs");
}
✅ Use Case: Closing database connections, releasing resources.

49. Will System.Exit() in try Block Execute finally Block? (⭐⭐)
🔹 No, System.Exit() immediately terminates the process.
Example:
try {
    Console.WriteLine("Try Block");
    System.Environment.Exit(0); // Exits program
} finally {
    Console.WriteLine("Will not execute");
}
✅ Use Case: Forceful termination.

50. Can You Return Multiple Values from a Function in C#? (⭐⭐)
🔹 Yes, using Tuple, out, or ValueTuple.
Example Using Tuple:
(Tuple<int, string>) GetDetails() => Tuple.Create(1, "Vishal");
✅ Use Case: Returning multiple results efficiently.

51. What is an Anonymous Type in C#? (⭐⭐)
🔹 A class without a name, created at runtime.
Example:
var person = new { Name = "Vishal", Age = 30 };
Console.WriteLine(person.Name);
✅ Use Case: Temporary objects.

52. Difference Between Task and Thread in .NET? (⭐⭐)
Feature	Task	Thread
Abstraction	Higher-level	Lower-level
Performance	Optimized	Requires manual control
Example:
Task.Run(() => Console.WriteLine("Task Execution"));

53. What is the yield Keyword Used for in C#? (⭐⭐)
🔹 Lazy evaluation in iterators.
Example:
IEnumerable<int> GetNumbers() {
    yield return 1;
    yield return 2;
}
✅ Use Case: Efficient data streaming.

54. Why Use lock Statement in C#? (⭐)
🔹 Prevents multiple threads from accessing a resource simultaneously.
Example:
private static readonly object obj = new object();

lock (obj) {
    Console.WriteLine("Thread Safe Code");
}
✅ Use Case: Thread synchronization.



