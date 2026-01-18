
# 📚 Table of Contents

1. [Design Patterns & Principles](#design-patterns--principles)
2. [Web API Authentication](#web-api-authentication)
3. [OOPS & Core C#](#oops--core-c)
4. [Exception Handling](#exception-handling)
5. [Memory & Conversion](#memory--conversion)
6. [Serialization & Generics](#serialization--generics)
7. [Delegates & Events](#delegates--events)
8. [Collections](#collections)
9. [Advanced Topics](#advanced-topics)
10. [Multithreading & Async](#multithreading--async)
11. [Database & Transactions](#database--transactions)
12. [Performance Optimization](#performance-optimization)
13. [Tricky Questions (10+ Years)](#tricky-questions-10-years)

---

# Design Patterns & Principles

---

## 1️⃣ Have You Worked on Any Design Pattern in C#? (***)

### ✅ Answer:

Yes, I have worked with multiple design patterns in real projects:

### 🔹 Singleton Pattern

Ensures only **one instance of a class** exists.

**Use Case:** Logging, Configuration Manager

---

### 🔹 Factory Pattern

Creates objects **without exposing creation logic**.

**Use Case:** Payment Gateway selection

---

### 🔹 Repository Pattern

Separates **data access logic from business logic**.

**Use Case:** Clean architecture with Entity Framework

---

### 🔹 Observer Pattern

Notifies subscribers when state changes.

**Use Case:** Event-based notifications

---

### 🔹 Dependency Injection (DI)

Provides dependencies externally instead of creating internally.

**Benefits:**

* Loose coupling
* Easy testing
* Maintainability

---

### 🔹 Adapter Pattern

Allows incompatible interfaces to work together.

**Use Case:** Integrating third-party APIs

---

## 2️⃣ Explain Design Principles in C# (SOLID) (***)

| Principle   | Meaning                                           |
| ----------- | ------------------------------------------------- |
| **S — SRP** | One class should have only one responsibility     |
| **O — OCP** | Open for extension, closed for modification       |
| **L — LSP** | Derived classes must replace base classes safely  |
| **I — ISP** | Avoid forcing clients to implement unused methods |
| **D — DIP** | Depend on interfaces not concrete classes         |

---

# Web API Authentication

---

## 3️⃣ How to Authenticate Web API? (**)

### ✅ Methods:

### 🔹 JWT Token Authentication

Stateless authentication using tokens.

### 🔹 OAuth 2.0

Used for third-party login (Google, Facebook).

### 🔹 Basic Authentication

Username/password via HTTP headers.

### 🔹 API Keys

Simple key-based authentication.

### 🔹 Windows Authentication

Used in intranet applications.

---

# OOPS & Core C#

---

## 4️⃣ Interface vs Abstract Class (***)

| Feature              | Interface            | Abstract Class            |
| -------------------- | -------------------- | ------------------------- |
| Methods              | Declaration only     | Can have implementation   |
| Fields               | ❌ No                 | ✅ Yes                     |
| Constructor          | ❌ No                 | ✅ Yes                     |
| Multiple Inheritance | ✅ Supported          | ❌ Not supported           |
| Usage                | Contract enforcement | Shared base functionality |

---

## 5️⃣ When to Use Interface vs Abstract Class (**)

### ✅ Use Interface when:

* Multiple classes share behavior contract
* You want loose coupling

### ✅ Use Abstract Class when:

* You want shared logic
* Partial implementation required

---

## 6️⃣ Exception Handling in C# (**)

Exception handling prevents application crashes.

```csharp
try {
   // Risky code
}
catch(Exception ex) {
   // Error handling
}
finally {
   // Cleanup code
}
```

### Common Exceptions:

* NullReferenceException
* IndexOutOfRangeException
* DivideByZeroException

---

## 7️⃣ Abstraction vs Encapsulation (*)

### 🔹 Abstraction

Hides implementation details.

### 🔹 Encapsulation

Protects data using access modifiers.

```csharp
public abstract class Vehicle {
   public abstract void Start(); 
}

public class Car : Vehicle {
   private int speed;
   public override void Start() { }
}
```

---

## 8️⃣ Private Constructor (***)

### Purpose:

* Prevent object creation
* Used in Singleton and Utility classes

```csharp
private Singleton() { }
```

---

# Memory & Conversion

---

## 9️⃣ Convert.ToString() vs ToString() (*)

| Method             | Behavior                      |
| ------------------ | ----------------------------- |
| Convert.ToString() | Returns empty string if null  |
| ToString()         | Throws NullReferenceException |

```csharp
object obj = null;
Convert.ToString(obj); // ""
obj.ToString(); // Exception
```

---

# Serialization & Generics

---

## 🔟 Serialization in C# (**)

Serialization converts objects to transferable format.

### Types:

* JSON
* XML
* Binary

```csharp
string json = JsonSerializer.Serialize(obj);
```

---

## 1️⃣1️⃣ Generics (***)

Allow type-safe reusable code.

```csharp
public class GenericClass<T> {
 public T Value { get; set; }
}
```

### Benefits:

* Performance
* Compile-time checking
* Code reuse

---

# Delegates & Events

---

## 1️⃣2️⃣ Delegates & Events (**)

### Delegate

References a method.

### Event

Notifies subscribers.

```csharp
public delegate void MyDelegate(string msg);

public event MyDelegate MyEvent;
```

---

# Collections

---

## 1️⃣3️⃣ Collections in C# (*)

| Collection | Use               |
| ---------- | ----------------- |
| List       | Dynamic array     |
| Dictionary | Key-value storage |
| Queue      | FIFO              |
| Stack      | LIFO              |
| HashSet    | Unique items      |

---

## 1️⃣4️⃣ Array vs ArrayList (⭐⭐)

| Feature     | Array | ArrayList |
| ----------- | ----- | --------- |
| Type Safe   | Yes   | No        |
| Performance | Fast  | Slower    |
| Size        | Fixed | Dynamic   |

✅ Use `List<T>` instead

---

# Advanced Topics

---

## 1️⃣5️⃣ Is string Value or Reference Type? (⭐)

### Answer:

String is a **reference type** but behaves like value type because it is **immutable**.

```csharp
string a="Hello";
string b=a;
a="World";
```

b remains "Hello"

---

## 1️⃣6️⃣ Reflection (⭐⭐)

Allows runtime inspection.

```csharp
Type t = typeof(string);
var methods = t.GetMethods();
```

### Use Cases:

* DI
* Serialization
* Plugin systems

---

## 1️⃣7️⃣ ref vs out (⭐⭐⭐⭐)

| Feature        | ref          | out           |
| -------------- | ------------ | ------------- |
| Initialization | Required     | Not required  |
| Usage          | Modify value | Return values |

---

## 1️⃣8️⃣ IEnumerable vs IQueryable (⭐⭐⭐⭐)

| Feature     | IEnumerable | IQueryable |
| ----------- | ----------- | ---------- |
| Execution   | Memory      | Database   |
| Performance | Slower      | Faster     |

---

## 1️⃣9️⃣ Garbage Collection (⭐⭐⭐)

### Generations:

* Gen 0 — Short-lived
* Gen 1 — Medium
* Gen 2 — Long-lived

---

## 2️⃣0️⃣ Overloading vs Overriding (⭐⭐)

| Feature     | Overloading | Overriding |
| ----------- | ----------- | ---------- |
| Inheritance | ❌           | ✅          |
| Signature   | Different   | Same       |

---

## 2️⃣1️⃣ Singleton Pattern (⭐⭐⭐)

```csharp
private static readonly Singleton instance = new();
```

### Use Cases:

* Logging
* Configuration

---

## 2️⃣2️⃣ Static Class (⭐⭐)

Used for helper methods.

```csharp
public static class MathHelper { }
```

---

## 2️⃣3️⃣ Static Constructor (⭐⭐)

Runs once per type.

---

## 2️⃣4️⃣ Types of Constructors (⭐)

* Default
* Parameterized
* Copy
* Static

---

## 2️⃣5️⃣ Inheritance (⭐)

Allows reuse of code.

---

## 2️⃣6️⃣ var vs dynamic (⭐⭐⭐)

| Feature      | var  | dynamic |
| ------------ | ---- | ------- |
| Compile Time | Yes  | No      |
| Performance  | Fast | Slow    |

---

# Multithreading & Async

---

## 2️⃣7️⃣ virtual & override (⭐)

Used for runtime polymorphism.

---

## 2️⃣8️⃣ Threading (⭐⭐)

Allows parallel execution.

---

## 2️⃣9️⃣ async & await (⭐⭐)

Non-blocking execution.

---

# Database & Transactions

---

## 3️⃣0️⃣ SqlBulkCopy (⭐)

Used for fast bulk insert.

---

## 3️⃣1️⃣ Transactions (⭐)

Ensures atomic operations.

---

## 3️⃣2️⃣ using keyword (⭐⭐⭐)

Auto resource cleanup.

---

# Performance Optimization

---

## 3️⃣3️⃣ const vs readonly (⭐⭐⭐)

| Feature        | const | readonly |
| -------------- | ----- | -------- |
| Compile time   | Yes   | No       |
| Runtime assign | ❌     | ✅        |

---

## 3️⃣4️⃣ sealed class (⭐⭐)

Prevents inheritance.

---

## 3️⃣5️⃣ Private Virtual Override (⭐)

❌ Not possible.

---

## 3️⃣6️⃣ CopyTo vs Clone (⭐)

Clone creates new array.

---

## 3️⃣7️⃣ Dispose vs Finalize (⭐⭐)

Dispose is faster and preferred.

---

## 3️⃣8️⃣ Object Pooling (⭐)

Improves memory reuse.

---

## 3️⃣9️⃣ Custom Exceptions (⭐)

Create domain-specific errors.

---

## 4️⃣0️⃣ Delegates (⭐⭐)

Used for callbacks.

---

# Tricky Questions (10+ Years)

---

## 4️⃣1️⃣ Nullable Types (⭐)

Allows value types to be null.

---

## 4️⃣2️⃣ is vs as (⭐)

Safe type checking.

---

## 4️⃣3️⃣ throw vs throw ex (⭐)

Use `throw` to preserve stack trace.

---

## 4️⃣4️⃣ Managed vs Unmanaged Code (⭐)

C# is managed code.

---

## 4️⃣5️⃣ continue vs break (⭐)

continue skips iteration
break exits loop

---

## 4️⃣6️⃣ Boxing & Unboxing (⭐)

Performance costly conversions.

---

## 4️⃣7️⃣ Namespace (⭐)

Logical code grouping.

---

## 4️⃣8️⃣ finally block (⭐)

Always executes cleanup.

---

## 4️⃣9️⃣ System.Exit() (⭐⭐)

finally block will NOT execute.

---

## 5️⃣0️⃣ Return Multiple Values (⭐⭐)

Use Tuple, out, ValueTuple.

---

## 5️⃣1️⃣ Anonymous Types (⭐⭐)

Temporary unnamed objects.

---

## 5️⃣2️⃣ Task vs Thread (⭐⭐)

Task is higher abstraction.

---

## 5️⃣3️⃣ yield keyword (⭐⭐)

Lazy data loading.

---

## 5️⃣4️⃣ lock keyword (⭐)

Thread synchronization.
 

Just say **YES** 👍
