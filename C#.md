📑 Table of Contents (C# Interview Questions 1–36)

### PART 1

* [1. Have you worked on Any Design Pattern in C#?](#1-have-you-worked-on-any-design-pattern-in-c)
* [2. Explain Design Principles in C# (SOLID)?](#2-explain-design-principles-in-c-solid)
* [3. How to Authenticate Web API?](#3-how-to-authenticate-web-api)
* [4. Difference Between Interface and Abstract Class?](#4-difference-between-interface-and-abstract-class)
* [5. When to use Interface and when to use Abstract Class?](#5-when-to-use-interface-and-when-to-use-abstract-class)
* [6. Exception Handling in C#?](#6-exception-handling-in-c)
* [7. Difference Between Data Abstraction and Encapsulation?](#7-difference-between-data-abstraction-and-encapsulation)
* [8. Explain Private Constructor? When is it used?](#8-explain-private-constructor-when-is-it-used)
* [9. Difference Between Convert.ToString() and .ToString()?](#9-difference-between-converttostring-and-tostring)
* [10. Serialization in C#?](#10-serialization-in-c)
* [11. Generics in C#?](#11-generics-in-c)
* [12. Events and Delegates in C#?](#12-events-and-delegates-in-c)
* [13. Collections in C#?](#13-collections-in-c)
* [14. Difference Between Array and ArrayList in C#?](#14-difference-between-array-and-arraylist-in-c)
* [15. Is string a Value Type or Reference Type?](#15-is-string-a-value-type-or-reference-type)
* [16. What is Reflection in C#?](#16-what-is-reflection-in-c)
* [17. Difference Between ref and out in C#?](#17-difference-between-ref-and-out-in-c)
* [18. Difference Between IEnumerable and IQueryable?](#18-difference-between-ienumerable-and-iqueryable)

---

### PART 2

* [19. Garbage Collection in C#?](#19-garbage-collection-in-c)
* [20. Explain Method Overloading vs Method Overriding?](#20-explain-method-overloading-vs-method-overriding)
* [21. Explain Singleton Design Pattern?](#21-explain-singleton-design-pattern)
* [22. When to Use a static Class?](#22-when-to-use-a-static-class)
* [23. Can We Create a Static Constructor?](#23-can-we-create-a-static-constructor)
* [24. Types of Constructors in C#?](#24-types-of-constructors-in-c)
* [25. Explain Inheritance in C#?](#25-explain-inheritance-in-c)
* [26. Difference Between var and dynamic in C#?](#26-difference-between-var-and-dynamic-in-c)
* [27. Explain virtual and override Keywords in C#?](#27-explain-virtual-and-override-keywords-in-c)
* [28. Explain Threading in C#?](#28-explain-threading-in-c)
* [29. Explain async and await in C#?](#29-explain-async-and-await-in-c)
* [30. How to Perform Bulk Insert in SQL from C#?](#30-how-to-perform-bulk-insert-in-sql-from-c)
* [31. What is a Transaction in C#?](#31-what-is-a-transaction-in-c)
* [32. What is using in C#?](#32-what-is-using-in-c)
* [33. Difference Between const and readonly in C#?](#33-difference-between-const-and-readonly-in-c)
* [34. What is a sealed Class in C#?](#34-what-is-a-sealed-class-in-c)
* [35. Can a Private Virtual Method Be Overridden?](#35-can-a-private-virtual-method-be-overridden)
* [36. Difference Between Array.CopyTo() and Array.Clone()?](#36-difference-between-arraycopyto-and-arrayclone)
* [37. Finalize() vs Dispose()](#37-what-is-the-difference-between-finalize-and-dispose-methods)

  ### PART 3

* [38. Object Pool](#38-what-is-an-object-pool-in-net)
* [39. Custom Exceptions](#39-what-are-custom-exceptions)
* [40. Delegates](#40-what-are-delegates)
* [41. Nullable Types](#41-how-to-use-nullable-types-in-net)
* [42. is vs as](#42-what-is-difference-between-is-and-as-operators-in-c)
* [43. throw vs throw ex](#43-what-is-difference-between-the-throw-and-throw-ex-in-net)
* [44. Managed vs Unmanaged](#44-is-c-code-is-managed-or-unmanaged-code)
* [45. continue vs break](#45-what-is-the-difference-between-continue-and-break-statements-in-c)
* [46. Boxing & Unboxing](#46-what-is-boxing-and-unboxing)
* [47. Namespace](#47-what-is-namespace-in-c)
* [48. finally Block](#48-why-to-use-finally-block-in-c)
* [49. System.Exit & finally](#49-if-i-writte-systemexit-in-try-block-will-the-execution-will-go-to-finally-block)
* [50. Multiple Return Values](#50-can-you-return-multiple-values-from-a-function-in-c-provide-some-examples)
* [51. Anonymous Type](#51-explain-anonymous-type-in-c)
* [52. Task vs Thread](#52-explain-the-difference-between-task-and-thread-in-net)
* [53. yield Keyword](#53-what-is-the-yield-keyword-used-for-in-c)
* [54. lock Statement](#54-why-to-use-lock-statement-in-c)

---

# 1️⃣ Have You Worked on Any Design Pattern in C#? (***)

### ✅ Interview Answer (Detailed)

Yes, I have used multiple design patterns in enterprise-level applications to improve **code reusability, scalability, maintainability, and loose coupling**.

Design patterns provide **standard solutions to recurring software design problems** and help in building clean architecture.

---

## 🔹 Singleton Pattern

### What it does:

Ensures **only one instance of a class exists globally**.

### Why we use it:

* Prevent multiple object creation
* Maintain centralized state
* Reduce memory usage

### Real-world usage:

* Logger service
* Configuration manager
* Application cache manager

### Example:

```csharp
public sealed class Singleton
{
    private static readonly Singleton instance = new Singleton();

    private Singleton() { }

    public static Singleton Instance => instance;
}
```

---

## 🔹 Factory Pattern

### What it does:

Creates objects **without exposing the object creation logic**.

### Why it is important:

* Removes tight coupling
* Supports Open/Closed principle
* Improves flexibility

### Real-world example:

Payment Gateway System:

Instead of hardcoding:

```csharp
new CreditCardPayment();
```

Use Factory:

```csharp
PaymentFactory.Create("UPI");
```

---

## 🔹 Repository Pattern

### Purpose:

Separates **business logic from database logic**.

### Benefits:

* Cleaner architecture
* Easier unit testing
* Centralized data operations

### Example Scenario:

Service layer calls repository instead of writing SQL queries directly.

---

## 🔹 Dependency Injection (DI)

### What it does:

Injects dependencies instead of creating objects manually.

### Benefits:

* Loose coupling
* Easy mocking
* Easy maintenance

Example:

```csharp
public OrderService(ILogger logger)
{
    _logger = logger;
}
```

---

## 🔹 Observer Pattern

### Purpose:

Notifies subscribers automatically when state changes.

### Example Use Case:

* Event notifications
* Stock price updates
* Messaging systems

---

## 🔹 Adapter Pattern

### Purpose:

Allows incompatible interfaces to work together.

### Example:

Integrating old legacy system API with new application interface.

---

# 2️⃣ Explain Design Principles in C# (SOLID) (***)

### ✅ Interview Explanation:

SOLID principles are **object-oriented design guidelines** that help in writing **maintainable, scalable, testable, and flexible code**.

---

## 🔹 S — Single Responsibility Principle (SRP)

### Meaning:

A class should have **only one responsibility** and **one reason to change**.

### Example:

❌ Wrong Design:

Invoice class handling calculation + printing + saving

✅ Correct Design:

* InvoiceCalculator
* InvoicePrinter
* InvoiceRepository

---

## 🔹 O — Open Closed Principle (OCP)

### Meaning:

Software entities should be:

✔ Open for extension
❌ Closed for modification

### Benefit:

New features can be added without breaking existing code.

---

## 🔹 L — Liskov Substitution Principle (LSP)

### Meaning:

Derived class must be able to replace base class without changing behavior.

### Example:

Bird → Fly()

Penguin cannot fly → Violates LSP.

---

## 🔹 I — Interface Segregation Principle (ISP)

### Meaning:

Do not force clients to implement unnecessary methods.

### Example:

Instead of:

```csharp
IWorker
```

Split into:

* IWorkable
* IFeedable

---

## 🔹 D — Dependency Inversion Principle (DIP)

### Meaning:

High-level modules should depend on **abstractions, not concrete classes**.

### Example:

Depend on:

```csharp
ILogger
```

Instead of:

```csharp
FileLogger
```

---

# 3️⃣ How to Authenticate Web API? (**)

### ✅ Interview Explanation:

Authentication is used to **verify the identity of the user or client** before allowing API access.

---

## 🔹 JWT Authentication (Most Common)

### Flow:

1. User logs in
2. Server generates token
3. Token stored on client
4. Token sent with every request

### Advantages:

* Stateless
* Fast
* Works well with microservices

---

## 🔹 OAuth 2.0

Used for third-party authentication.

### Example:

* Google Login
* Facebook Login
* GitHub Authentication

---

## 🔹 API Key Authentication

Used for:

* External public APIs
* Partner integrations

---

## 🔹 Windows Authentication

Used mainly in:

* Internal enterprise applications
* Intranet systems

---

# 4️⃣ Difference Between Interface and Abstract Class (***)

### ✅ Interview Explanation:

Both are used for **abstraction**, but their purpose and capabilities differ.

---

| Feature              | Interface   | Abstract Class        |
| -------------------- | ----------- | --------------------- |
| Implementation       | No          | Yes (partial)         |
| Multiple Inheritance | Supported   | Not Supported         |
| Fields               | Not Allowed | Allowed               |
| Constructor          | Not Allowed | Allowed               |
| Purpose              | Contract    | Base behavior sharing |

---

### Practical Usage:

### Use Interface:

* When multiple classes need same contract
* When loose coupling required

### Use Abstract Class:

* When base logic needs sharing
* When common behavior exists

---

# 5️⃣ When to Use Interface vs Abstract Class (**)

### Use Interface When:

* You need multiple inheritance
* You want plug-and-play architecture
* You want dependency injection support

---

### Use Abstract Class When:

* You want default implementation
* You want to share base logic
* You want protected members

---

# 6️⃣ Exception Handling in C# (**)

### ✅ Interview Explanation:

Exception handling prevents application crashes and allows us to **gracefully handle runtime errors**.

---

### try-catch-finally Structure:

```csharp
try
{
    // Risky code
}
catch(Exception ex)
{
    // Handle exception
}
finally
{
    // Cleanup code
}
```

---

### Why finally is important:

* Closes database connections
* Releases memory
* Frees file handles

---

### Real-world Errors:

* Database timeout
* File not found
* Network failure

---

# 7️⃣ Difference Between Abstraction and Encapsulation (*)

### Abstraction:

Hides implementation complexity and exposes **only essential features**.

Example:

Interfaces and abstract classes.

---

### Encapsulation:

Protects data using **private fields and public properties**.

---

### Interview Tip:

Abstraction → Design level
Encapsulation → Implementation level

---

# 8️⃣ Explain Private Constructor (***)

### What it means:

Private constructor **prevents external object creation**.

---

### Why we use it:

* Singleton pattern
* Static utility classes
* Controlled object creation

---

### Example:

```csharp
private Singleton() { }
```

---

# 9️⃣ Convert.ToString() vs ToString() (*)

### Key Difference:

`Convert.ToString()` is safer.

---

### Example:

```csharp
object obj = null;

Convert.ToString(obj); // Returns ""
obj.ToString(); // Throws exception
```

---

### Interview Point:

Always use `Convert.ToString()` when null safety is required.

---

# 🔟 Serialization in C# (**)

### Meaning:

Serialization converts an object into **JSON, XML or Binary format** for:

* API communication
* File storage
* Caching

---

### Example:

```csharp
string json = JsonSerializer.Serialize(person);
```

---

### Real-world Usage:

* Web API response
* Saving object state
* Distributed systems

---

# 1️⃣1️⃣ Generics in C# (***)

### What are Generics:

Generics allow us to write **type-safe, reusable and performance-optimized code**.

---

### Example:

```csharp
public class GenericClass<T>
{
    public T Value { get; set; }
}
```

---

### Benefits:

* Compile-time type safety
* No boxing/unboxing
* Reusable components

---

# 1️⃣2️⃣ Delegates and Events (**)

### Delegate:

A delegate is a **type-safe reference to a method**.

---

### Event:

An event is a **notification mechanism** built on delegates.

---

### Real-world Use:

* Button click events
* Notification systems
* Messaging services

---

# 1️⃣3️⃣ Collections in C# (*)

### Purpose:

Collections store and manage **groups of related objects**.

---

### Common Collections:

| Type       | Purpose           |
| ---------- | ----------------- |
| List       | Dynamic array     |
| Dictionary | Key-value storage |
| Queue      | FIFO              |
| Stack      | LIFO              |
| HashSet    | Unique items      |

---

# 1️⃣4️⃣ Difference Between Array and ArrayList (⭐⭐)

### Key Differences:

| Feature     | Array  | ArrayList |
| ----------- | ------ | --------- |
| Type Safety | Strong | Weak      |
| Performance | Faster | Slower    |
| Size        | Fixed  | Dynamic   |

---

### Interview Tip:

Always prefer:

```csharp
List<T>
```

Instead of ArrayList.

---

# 1️⃣5️⃣ Is string Value Type or Reference Type? (⭐)

### Interview Explanation:

String is technically a **reference type**, but it behaves like a value type because it is **immutable**.

---

### Example:

```csharp
string s1 = "Hello";
string s2 = s1;

s1 = "World";
```

`s2` remains `"Hello"`

---

### Reason:

New memory is created instead of modifying existing value.

---

# 1️⃣6️⃣ Reflection in C# (⭐⭐)

### What is Reflection:

Reflection allows us to **inspect assemblies, types, methods and properties at runtime**.

---

### Example:

```csharp
Type type = typeof(string);
var methods = type.GetMethods();
```

---

### Real-world Use:

* Dependency Injection containers
* Unit testing frameworks
* Serialization libraries

---

# 1️⃣7️⃣ Difference Between ref and out (⭐⭐⭐⭐)

### Explanation:

Both pass variables by reference but behave differently.

---

| Feature        | ref          | out                    |
| -------------- | ------------ | ---------------------- |
| Initialization | Required     | Not Required           |
| Purpose        | Modify value | Return multiple values |

---

### Example:

```csharp
void Test(ref int a, out int b)
{
    a += 5;
    b = 10;
}
```

---

# 1️⃣8️⃣ IEnumerable vs IQueryable (⭐⭐⭐⭐)

### Interview Explanation:

Both are used for querying collections but execution differs.

---

### IEnumerable:

* Executes in memory
* Suitable for small datasets

---

### IQueryable:

* Executes on database server
* Generates SQL query
* Better performance for large data

---

### Example:

```csharp
IQueryable<Employee> data = db.Employees;
```

---
# ✅ PART 1 Completed (1–18)


# 📘 PART 2 — Programming & .NET Interview Guide (19–36)

---

## **19. What are OOP Principles? Explain with Examples**

### 📌 Definition

Object-Oriented Programming (OOP) is a programming paradigm that organizes software around **objects** instead of functions and logic.

### ✅ Four Core Principles

### **1️⃣ Encapsulation**

* Wrapping data + behavior into a single unit (class)
* Restricts direct access using access modifiers

**Example:**

```csharp
class Account
{
    private double balance;

    public void Deposit(double amount)
    {
        balance += amount;
    }
}
```

### **2️⃣ Inheritance**

* Child class reuses parent class behavior

```csharp
class Vehicle { }
class Car : Vehicle { }
```

### **3️⃣ Polymorphism**

* Same method behaves differently

```csharp
virtual void Print()
override void Print()
```

### **4️⃣ Abstraction**

* Shows only necessary details

```csharp
interface IPayment
{
   void Pay();
}
```

### 🎯 Interviewer Tips

* Always explain with **real-life analogy** (ATM, Vehicle, Payment Gateway)
* Mention **maintainability and scalability benefits**

---

## **20. Explain SOLID Principles**

### 📌 Definition

SOLID principles help design **scalable, maintainable, and testable software**.

---

### **S — Single Responsibility Principle**

One class = One responsibility

❌ Bad:

* User class handling DB + validation

✅ Good:

* UserService
* UserRepository

---

### **O — Open/Closed Principle**

Open for extension, closed for modification.

Use interfaces and inheritance.

---

### **L — Liskov Substitution Principle**

Derived class should replace base class without breaking behavior.

---

### **I — Interface Segregation**

Many small interfaces > One big interface.

---

### **D — Dependency Inversion**

Depend on abstractions, not concrete classes.

```csharp
IPayment payment = new CardPayment();
```

---

### 🎯 Interviewer Tip

Say:

> "SOLID reduces tight coupling and improves unit testing."

---

## **21. Difference Between Interface and Abstract Class**

| Feature               | Interface     | Abstract Class  |
| --------------------- | ------------- | --------------- |
| Multiple Inheritance  | ✅ Yes         | ❌ No            |
| Method Implementation | ❌ Not allowed | ✅ Allowed       |
| Fields                | ❌ No          | ✅ Yes           |
| Constructor           | ❌ No          | ✅ Yes           |
| Performance           | Faster        | Slightly slower |

---

### ✅ When to Use Interface

* Multiple inheritance
* Contract definition

### ✅ When to Use Abstract Class

* Common base behavior

---

## **22. IEnumerable vs IQueryable**

### 📌 IEnumerable

* In-memory collection
* Executes query on client side

### 📌 IQueryable

* Database-level execution
* Translates to SQL

---

### Example:

```csharp
var list = db.Users.Where(x => x.Age > 25);
```

If using IQueryable → SQL runs in DB
If IEnumerable → Data fetched first, then filtered

---

### 🎯 Interview Tip

Always say:

> "Use IQueryable for large DB operations to improve performance."

---

## **23. What is Deferred Execution in LINQ?**

### 📌 Definition

LINQ queries execute only when result is enumerated.

---

### Example:

```csharp
var result = users.Where(x => x.Age > 25);

// Query runs here:
foreach(var u in result)
```

---

### Benefits:

* Performance optimization
* Query chaining

---

### 🎯 Tip

Mention `.ToList()` forces execution immediately.

---

## **24. Explain async and await**

### 📌 Definition

Used for **non-blocking asynchronous programming**.

---

### Example:

```csharp
public async Task GetData()
{
    await Task.Delay(2000);
}
```

---

### Benefits:

* UI responsiveness
* Better scalability
* Thread not blocked

---

### Important Points:

* await releases thread
* async improves performance under load

---

## **25. Difference Between Task and Thread**

| Feature     | Task                  | Thread    |
| ----------- | --------------------- | --------- |
| Level       | High-level            | Low-level |
| Management  | Managed by ThreadPool | Manual    |
| Performance | Efficient             | Heavy     |
| Recommended | ✅ Yes                 | ❌ Avoid   |

---

### Example:

```csharp
Task.Run(() => DoWork());
```

---

### 🎯 Tip

Say:

> "Task is preferred in modern .NET apps."

---

## **26. Multithreading vs Parallel Programming**

### Multithreading:

* Multiple threads
* Manual management

### Parallel Programming:

* Automatic thread management
* Uses Task Parallel Library (TPL)

---

### Example:

```csharp
Parallel.For(0, 10, i => {});
```

---

### Interview Tip

Parallel = easier and safer

---

## **27. What is Garbage Collection?**

### 📌 Definition

Automatic memory cleanup of unused objects.

---

### GC Generations:

| Generation | Description         |
| ---------- | ------------------- |
| Gen 0      | Short-lived objects |
| Gen 1      | Medium              |
| Gen 2      | Long-lived          |

---

### Benefits:

* Prevents memory leaks
* Automatic memory handling

---

### 🎯 Tip

Mention:

> "Dispose unmanaged resources manually using using keyword."

---

## **28. Value Types vs Reference Types**

### Value Type:

* Stored in Stack
* Copy by value

Examples:

* int, double, struct

---

### Reference Type:

* Stored in Heap
* Copy by reference

Examples:

* class, array, object

---

### Interview Trick:

Modifying reference affects original object.

---

## **29. Boxing and Unboxing**

### Boxing:

Value → Object

```csharp
int a = 10;
object b = a;
```

### Unboxing:

Object → Value

```csharp
int c = (int)b;
```

---

### Performance Impact:

* Boxing causes memory overhead

---

### Tip:

Avoid boxing in performance-critical apps.

---

## **30. What are Delegates? Func and Action?**

### 📌 Delegate:

Pointer to method.

```csharp
delegate void Print();
```

---

### Func:

* Returns value

```csharp
Func<int,int> square = x => x*x;
```

---

### Action:

* No return value

```csharp
Action<string> print = msg => Console.WriteLine(msg);
```

---

### Interview Tip:

Delegates enable callbacks and events.

---

## **31. What are Events in C#?**

### 📌 Definition

Event notifies subscribers when something happens.

---

### Example:

```csharp
public event Action OnPaymentDone;
```

---

### Use Cases:

* Button click
* Notification system

---

### Tip:

Say:

> "Events implement Observer pattern."

---

## **32. What is Dependency Injection (DI)?**

### 📌 Definition

Injecting object dependencies instead of creating them manually.

---

### Example:

❌ Bad:

```csharp
new PaymentService();
```

✅ Good:

```csharp
IPayment payment;
```

---

### Benefits:

* Loose coupling
* Easy testing
* Better maintainability

---

## **33. Explain Factory and Singleton Patterns**

---

### Singleton:

Only one instance exists.

```csharp
private static instance;
```

Use Case:

* Logging
* Configuration

---

### Factory:

Object creation centralized.

Use Case:

* Payment Gateway selection

---

### Interview Tip:

Mention real business use.

---

## **34. What is REST API?**

### 📌 Definition

REST = Representational State Transfer.

Uses HTTP protocol.

---

### Key Principles:

* Stateless
* Resource-based URLs
* Uses HTTP verbs

---

### Example:

```
GET /api/users
POST /api/users
```

---

## **35. Authentication vs Authorization**

### Authentication:

Who are you?

(Login)

---

### Authorization:

What can you access?

(Role based access)

---

### JWT Token Flow:

Login → Token → API Access

---

### Interview Tip:

Explain with Admin/User roles.

---

## **36. What is Caching?**

### 📌 Definition

Storing frequently used data in memory.

---

### Types:

### In-Memory Cache:

* Fast
* App-level

### Distributed Cache:

* Redis
* Multi-server support

---

### Benefits:

* Improves performance
* Reduces DB calls

---

### Interview Tip:

Say:

> "Caching is critical for high traffic applications."

---

# ✅ PART 2 Completed (19–36)

---

# 📘 C# Interview Questions & Answers — PART 3 (Advanced)

 
---

## 37. What is the difference between Finalize() and Dispose() methods?

### 📌 Definition

Both are used to **release unmanaged resources**, but they differ in **who calls them and when**.

---

### 🔹 Finalize()

* Called automatically by **Garbage Collector**
* Non-deterministic (no guarantee of when it runs)
* Slows down performance
* Used as backup cleanup

---

### 🔹 Dispose()

* Called manually by developer
* Deterministic cleanup
* Implemented using `IDisposable`
* Faster and recommended

---

### ✅ Comparison Table

| Feature       | Finalize()        | Dispose()   |
| ------------- | ----------------- | ----------- |
| Called By     | Garbage Collector | Developer   |
| Timing        | Unpredictable     | Immediate   |
| Performance   | Slower            | Faster      |
| Best Practice | Avoid if possible | Recommended |

---

### ✅ Example

```csharp
class MyResource : IDisposable
{
    public void Dispose()
    {
        Console.WriteLine("Dispose called");
        GC.SuppressFinalize(this);
    }

    ~MyResource()
    {
        Console.WriteLine("Finalize called");
    }
}
```

---

### 🎯 Interview Tip

👉 Always prefer **Dispose + using block** instead of Finalize.

---

## 38. What is an object pool in .NET?

### 📌 Definition

Object Pool is a **design pattern** that **reuses objects instead of creating new ones repeatedly**.

---

### 🔹 Why Needed?

Creating objects repeatedly:

* Consumes memory
* Creates GC pressure
* Reduces performance

---

### 🔹 How Pool Works

1. Create object once
2. Reuse it
3. Return back to pool

---

### ✅ Real Example

Database connections:

```text
Open connection → Use → Return to pool → Reuse
```

---

### 🎯 Benefits

✔ Faster performance
✔ Reduced memory allocation
✔ Lower garbage collection

---

## 39. What are Custom Exceptions?

### 📌 Definition

Custom exceptions are **user-defined exception classes** created for **business-specific errors**.

---

### 🔹 Why Use?

Built-in exceptions are generic.
Custom exceptions provide:

* Clear meaning
* Better debugging
* Business error separation

---

### ✅ Example

```csharp
public class InvalidAgeException : Exception
{
    public InvalidAgeException(string message) : base(message) { }
}
```

Usage:

```csharp
throw new InvalidAgeException("Age must be above 18");
```

---

### 🎯 Interview Tip

👉 Always inherit from `Exception` class.

---

## 40. What are delegates?

### 📌 Definition

Delegate is a **type-safe function pointer** that holds reference to a method.

---

### 🔹 Why Delegates?

Used for:

* Callbacks
* Event handling
* Passing methods as parameters

---

### ✅ Example

```csharp
public delegate void Notify(string msg);

Notify obj = Message;

static void Message(string msg)
{
    Console.WriteLine(msg);
}
```

---

### 🎯 Real Use Case

Events internally use delegates.

---

## 41. How to use nullable types in .Net?

### 📌 Definition

Nullable types allow **value types to store null**.

---

### 🔹 Syntax

```csharp
int? age = null;
```

---

### 🔹 Access Value

```csharp
if(age.HasValue)
{
   Console.WriteLine(age.Value);
}
```

---

### 🔹 Use Case

✔ Database NULL values
✔ Optional fields

---

### 🎯 Interview Tip

Use null-coalescing operator:

```csharp
int result = age ?? 0;
```

---

## 42. What is difference between "is" and "as" operators in C#?

### 📌 is Operator

* Checks type compatibility
* Returns true/false

```csharp
if(obj is string)
```

---

### 📌 as Operator

* Safe casting
* Returns null if failed

```csharp
string s = obj as string;
```

---

### ✅ Comparison

| Feature     | is      | as             |
| ----------- | ------- | -------------- |
| Return Type | Boolean | Object or null |
| Casting     | No      | Yes            |
| Exception   | Never   | Never          |

---

## 43. What is difference between "throw" and "throw ex" in .NET?

### 🔹 throw

Preserves original stack trace.

### 🔹 throw ex

Resets stack trace ❌ (Bad Practice)

---

### ✅ Example

```csharp
catch(Exception ex)
{
   throw;    // Good
   // throw ex; ❌
}
```

---

### 🎯 Interview Tip

Always use **throw** not throw ex.

---

## 44. Is C# code is managed or unmanaged code?

### 📌 Answer

C# is **Managed Code**.

---

### 🔹 Managed Code

✔ Runs under CLR
✔ Automatic memory management
✔ Garbage Collection
✔ Type safety

---

### 🔹 Unmanaged Code

C/C++ programs:

* Manual memory handling
* No runtime safety

---

## 45. What is the difference between continue and break statements in C#?

### 📌 continue

Skips current iteration.

### 📌 break

Terminates loop completely.

---

### ✅ Example

```csharp
for(int i=1;i<=5;i++)
{
 if(i==3) continue;
 Console.WriteLine(i);
}
```

Output:

```
1 2 4 5
```

---

## 46. What is Boxing and Unboxing?

### 📌 Boxing

Converts value type → object

```csharp
int a = 10;
object obj = a;
```

---

### 📌 Unboxing

Object → Value type

```csharp
int b = (int)obj;
```

---

### 🔹 Problem

Boxing causes:

❌ Performance overhead
❌ Heap allocation

---

### 🎯 Interview Tip

Avoid boxing in loops.

---

## 47. What is namespace in C#?

### 📌 Definition

Namespace organizes classes and prevents naming conflicts.

---

### ✅ Example

```csharp
namespace BankingApp
{
   class Account { }
}
```

---

### 🎯 Benefits

✔ Code organization
✔ Avoid class name collision
✔ Modular design

---

## 48. Why to use finally block in C#?

### 📌 Purpose

finally block **always executes** regardless of exception.

---

### 🔹 Used For

✔ Closing DB connections
✔ Releasing files
✔ Cleaning memory

---

### ✅ Example

```csharp
try { }
finally
{
   connection.Close();
}
```

---

## 49. If I write System.Exit in Try block will the execution go to Finally Block?

### ❌ Answer: NO

System.Exit **terminates process immediately**.

---

### ✅ Example

```csharp
try
{
  System.Environment.Exit(0);
}
finally
{
 Console.WriteLine("Will NOT execute");
}
```

---

### 🎯 Interview Tip

Different from return statement.

---

## 50. Can you return multiple values from a function in C#?

### ✅ Yes — Multiple Ways

---

### 🔹 Using Tuple

```csharp
var result = (1, "Vishal");
```

---

### 🔹 Using out parameters

```csharp
void GetData(out int a, out int b)
```

---

### 🔹 Using Class/Object

Return DTO object.

---

### 🎯 Best Practice

Use **ValueTuple** or DTO.

---

## 51. Explain Anonymous type in C#

### 📌 Definition

Anonymous types are **temporary unnamed objects** created at runtime.

---

### ✅ Example

```csharp
var emp = new { Name="Vishal", Age=30 };
```

---

### 🔹 Features

✔ Read-only
✔ No class definition
✔ Used in LINQ

---

## 52. Explain the difference between Task and Thread in .NET

### 📌 Thread

* Low-level
* Heavy resource
* Manual management

---

### 📌 Task

* High-level abstraction
* Thread pool based
* Optimized scheduling

---

### ✅ Example

```csharp
Task.Run(() => DoWork());
```

---

### 🎯 Interview Tip

Always prefer **Task over Thread**.

---

## 53. What is the yield keyword used for in C#?

### 📌 Definition

yield enables **lazy execution** of collections.

---

### ✅ Example

```csharp
IEnumerable<int> Numbers()
{
 yield return 1;
 yield return 2;
}
```

---

### 🔹 Benefits

✔ Memory efficient
✔ Faster streaming
✔ Deferred execution

---

## 54. Why to use lock statement in C#?

### 📌 Purpose

lock ensures **thread safety**.

---

### 🔹 Problem Without lock

Multiple threads modify shared resource → Data corruption.

---

### ✅ Example

```csharp
lock(obj)
{
 counter++;
}
```

---

### 🎯 Interview Tip

Avoid locking on:

❌ this
❌ string
❌ public objects

Use **private static object**.

 
