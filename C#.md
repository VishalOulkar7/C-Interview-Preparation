# C-Interview-Preparation



## ⭐ Difficulty Legend

* ⭐ Basic
* ⭐⭐ Intermediate
* ⭐⭐⭐ Advanced
* ⭐⭐⭐⭐ Expert

---

# 1. Have You Worked on Any Design Pattern in C#? (⭐⭐⭐)

### ✅ Answer:

Yes, I have worked with several design patterns such as:

* **Singleton Pattern** – Ensures only one instance of a class
* **Factory Pattern** – Creates objects without exposing creation logic
* **Repository Pattern** – Used in data access abstraction
* **Observer Pattern** – Used for event notifications
* **Dependency Injection (DI)** – External dependency management
* **Adapter Pattern** – Allows incompatible interfaces to work together

---

# 2. Explain SOLID Design Principles (⭐⭐⭐)

| Principle | Description                                                                      |
| --------- | -------------------------------------------------------------------------------- |
| SRP       | Single Responsibility Principle – One reason to change                           |
| OCP       | Open/Closed Principle – Open for extension, closed for modification              |
| LSP       | Liskov Substitution Principle – Derived classes must replace base classes safely |
| ISP       | Interface Segregation Principle – Avoid fat interfaces                           |
| DIP       | Dependency Inversion Principle – Depend on abstractions                          |

---

# 3. How to Authenticate Web API? (⭐⭐)

### ✅ Methods:

* JWT Token Authentication
* OAuth 2.0
* Basic Authentication
* API Keys
* Windows Authentication

---

# 4. Interface vs Abstract Class (⭐⭐⭐)

| Feature              | Interface           | Abstract Class             |
| -------------------- | ------------------- | -------------------------- |
| Methods              | Declaration only    | Can contain implementation |
| Fields               | Not allowed         | Allowed                    |
| Constructor          | Not allowed         | Allowed                    |
| Multiple Inheritance | Supported           | Not supported              |
| Use Case             | Contract definition | Shared base logic          |

---

# 5. When to Use Interface vs Abstract Class? (⭐⭐)

### ✅ Interface:

* When defining contracts
* Multiple inheritance required

### ✅ Abstract Class:

* When sharing common behavior
* Partial implementation needed

---

# 6. Exception Handling in C# (⭐⭐)

```csharp
try
{
    // Risky code
}
catch (Exception ex)
{
    // Handle exception
}
finally
{
    // Cleanup
}
```

### Common Exceptions:

* NullReferenceException
* IndexOutOfRangeException
* DivideByZeroException

---

# 7. Abstraction vs Encapsulation (⭐)

```csharp
public abstract class Vehicle
{
    public abstract void Start();   // Abstraction
}

public class Car : Vehicle
{
    private int speed;              // Encapsulation
    public override void Start() { }
}
```

---

# 8. Private Constructor (⭐⭐⭐)

### ✅ Use Cases:

* Singleton Pattern
* Utility Classes

```csharp
public class Singleton
{
    private static Singleton instance;

    private Singleton() { }

    public static Singleton GetInstance()
    {
        return instance ??= new Singleton();
    }
}
```

---

# 9. Convert.ToString() vs ToString() (⭐)

| Method             | Behavior                 |
| ------------------ | ------------------------ |
| .ToString()        | Throws exception if null |
| Convert.ToString() | Returns empty string     |

```csharp
object obj = null;

Convert.ToString(obj); // ""
obj.ToString();        // Exception
```

---

# 10. Serialization in C# (⭐⭐)

```csharp
using System.Text.Json;

Person p = new Person { Name = "John", Age = 30 };
string json = JsonSerializer.Serialize(p);
```

### Types:

* JSON
* XML
* Binary

---

# 11. Generics in C# (⭐⭐⭐)

```csharp
public class GenericClass<T>
{
    public T Value { get; set; }
}
```

### Benefits:

* Type safety
* Reusability
* Performance

---

# 12. Events and Delegates (⭐⭐)

```csharp
public delegate void MyDelegate(string msg);

public class EventExample
{
    public event MyDelegate MyEvent;

    public void Trigger()
    {
        MyEvent?.Invoke("Triggered");
    }
}
```

---

# 13. Collections in C# (⭐)

### Common Types:

* List<T>
* Dictionary<TKey,TValue>
* Queue
* Stack
* HashSet

```csharp
List<int> nums = new List<int> {1,2,3};
nums.Add(4);
```

---

# 14. Array vs ArrayList (⭐⭐)

| Feature             | Array          | ArrayList          |
| ------------------- | -------------- | ------------------ |
| Type Safety         | Strongly typed | Object based       |
| Performance         | Fast           | Slower             |
| Size                | Fixed          | Dynamic            |
| Namespace           | System         | System.Collections |
| Generic Alternative | T[]            | List<T>            |

```csharp
int[] numbers = {1,2,3};

ArrayList list = new ArrayList();
list.Add(1);
list.Add("Hello");
```

✅ Best Practice: Always use `List<T>`

---

# 15. Is String Value Type or Reference Type? (⭐)

String is reference type but **immutable**.

```csharp
string s1 = "Hello";
string s2 = s1;

s1 = "World";

Console.WriteLine(s2); // Hello
```

---

# 16. Reflection in C# (⭐⭐)

```csharp
Type type = typeof(string);
var methods = type.GetMethods();
```

### Use Cases:

* Dependency Injection
* Serialization
* Runtime inspection

---

# 17. ref vs out (⭐⭐⭐⭐)

| Feature        | ref             | out          |
| -------------- | --------------- | ------------ |
| Initialization | Required        | Not required |
| Purpose        | Modify existing | Return value |

```csharp
void Test(ref int a, out int b)
{
    a += 10;
    b = 20;
}
```

---

# 18. IEnumerable vs IQueryable (⭐⭐⭐⭐)

| Feature     | IEnumerable | IQueryable     |
| ----------- | ----------- | -------------- |
| Execution   | In-memory   | Database       |
| Performance | Slower      | Optimized      |
| Use Case    | Small data  | Large datasets |

---

# 19. Garbage Collection (⭐⭐⭐)

### GC Generations:

* Gen 0 → Short lived
* Gen 1 → Medium
* Gen 2 → Long lived

```csharp
GC.Collect(); // Not recommended
```

---

# 20. Method Overloading vs Overriding (⭐⭐)

| Feature     | Overloading  | Overriding |
| ----------- | ------------ | ---------- |
| Signature   | Different    | Same       |
| Inheritance | Not required | Required   |

---

# 21. Singleton Pattern (⭐⭐⭐)

```csharp
public sealed class Singleton
{
    private static readonly Singleton instance = new Singleton();
    private Singleton() { }

    public static Singleton Instance => instance;
}
```

---

# 22. Static Class (⭐⭐)

```csharp
public static class MathHelper
{
    public static int Square(int x) => x * x;
}
```

---

# 23. Static Constructor (⭐⭐)

```csharp
class Example
{
    static Example()
    {
        Console.WriteLine("Called once");
    }
}
```

---

# 24. Types of Constructors (⭐)

| Type          | Purpose             |
| ------------- | ------------------- |
| Default       | No parameters       |
| Parameterized | Takes input         |
| Copy          | Copy object         |
| Static        | Init static members |

---

# 25. Inheritance (⭐)

```csharp
class Animal { }
class Dog : Animal { }
```

---

# 26. var vs dynamic (⭐⭐⭐)

| Feature     | var          | dynamic |
| ----------- | ------------ | ------- |
| Resolution  | Compile-time | Runtime |
| Performance | Fast         | Slow    |

---

# 27. virtual vs override (⭐)

```csharp
class Base
{
    public virtual void Show() {}
}

class Derived : Base
{
    public override void Show() {}
}
```

---

# 28. Threading (⭐⭐)

```csharp
Thread t = new Thread(Print);
t.Start();
```

---

# 29. async / await (⭐⭐)

```csharp
await Task.Delay(2000);
```

---

# 30. SqlBulkCopy (⭐)

```csharp
SqlBulkCopy bulk = new SqlBulkCopy(conn);
bulk.WriteToServer(table);
```

---

# 31. Transaction (⭐)

```csharp
using(TransactionScope scope)
{
    scope.Complete();
}
```

---

# 32. using Statement (⭐⭐⭐)

```csharp
using(StreamWriter sw = new StreamWriter("file.txt"))
{
}
```

---

# 33. const vs readonly (⭐⭐⭐)

| Feature    | const        | readonly         |
| ---------- | ------------ | ---------------- |
| Assignment | Compile time | Constructor time |

---

# 34. sealed Class (⭐⭐)

```csharp
sealed class Secure {}
```

---

# 35. Can Private Virtual Be Overridden? (⭐)

❌ No — private methods are not accessible.

---

# 36. Clone vs CopyTo (⭐)

| Feature           | Clone | CopyTo |
| ----------------- | ----- | ------ |
| Creates new array | Yes   | No     |

---

# 37. Finalize vs Dispose (⭐⭐)

| Feature   | Finalize | Dispose   |
| --------- | -------- | --------- |
| Called by | GC       | Developer |

---

# 38. Object Pool (⭐)

Used for **reusing expensive objects**.

---

# 39. Custom Exception (⭐)

```csharp
class MyException : Exception {}
```

---

# 40. Delegate (⭐⭐)

```csharp
public delegate void MyDelegate(string msg);
```

---

# 41. Nullable Types (⭐)

```csharp
int? num = null;
```

---

# 42. is vs as (⭐)

```csharp
obj is string
obj as string
```

---

# 43. throw vs throw ex (⭐)

| Feature     | throw     | throw ex |
| ----------- | --------- | -------- |
| Stack Trace | Preserved | Lost     |

---

# 44. Managed vs Unmanaged Code (⭐)

C# → Managed
C++ → Unmanaged

---

# 45. break vs continue (⭐)

| Keyword  | Behavior       |
| -------- | -------------- |
| break    | Exit loop      |
| continue | Skip iteration |

---

# 46. Boxing & Unboxing (⭐)

```csharp
object o = 10; // Boxing
int x = (int)o; // Unboxing
```

---

# 47. Namespace (⭐)

```csharp
namespace MyApp {}
```

---

# 48. finally Block (⭐)

Always executes.

---

# 49. Environment.Exit() (⭐⭐)

❌ finally will NOT execute.

---

# 50. Multiple Return Values (⭐⭐)

```csharp
return (1, "Vishal");
```

---

# 51. Anonymous Type (⭐⭐)

```csharp
var emp = new { Name="Vishal", Age=30 };
```

---

# 52. Task vs Thread (⭐⭐)

| Feature | Task | Thread |
| ------- | ---- | ------ |
| Level   | High | Low    |

---

# 53. yield Keyword (⭐⭐)

```csharp
yield return 1;
```

---

# 54. lock Statement (⭐)

```csharp
lock(obj)
{
}
```

---

# ✅ END OF README

---

If you want, I can also:

✅ Add **Table of Contents with clickable links**
✅ Add **Badges + GitHub styling header**
✅ Convert this into **PDF Interview Notes**
✅ Optimize for **SEO + Recruiter friendly GitHub repo**
✅ Separate into **Beginner / Intermediate / Senior folders**

Just tell me 👍



