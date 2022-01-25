# Chapter 05 - Access Modifiers

---

## Definition
Consider this line of code:

```csharp
public string color;
```

The `public` keyword is an access modifier. This is used to set the access level (visibility) for a class, field, method, or property.

## Modifiers Table

| Modifier | Description |
|---|---|
| `public` |  Accessible to all classes. |
| `private` | Only accessible within the same class. |
| `protected` | Accessible within the same class, or any children classes that inherit. |
| `internal` | Only accessible from within its own assembly. |

There are also two possible combinations:

```csharp
protected internal
private protected
```

## Private Modifier
If you declare a field with a `private` access modifier, it can only be accessed from within the same class.

```csharp
class Car
{
	private string model = "Mustang";
	
	static void Main(string[] args)
	{
		Car myObj = new Car();
		Console.WriteLine(myObj.model);
	}
}
```

\
If you try to access it from outside the class, there will be an error.

```csharp
class Car
{
	private string model = "Mustang";
}

class Program
{
	static void Main(string[] args)
	{
		Car myObj = new Car();
		Console.WriteLine(myObj.model);		// Error
	}
}
```

\
The console will output:

```
'Car.model' is inaccessible due to its protection level
The field 'Car.model' is assigned but its value is never used
```

## Public Modifier
If you declare a field with a `public` access modifier, it is accessible to all classes.

```csharp
class Car
{
	public string model = "Mustang";
}

class Program
{
	static void Main(string[] args)
	{
		Car myObj = new Car();
		
		Console.WriteLine(myObj.model);
		Console.WriteLine("This is allowed.");
	}
}
```

## Reason
* Access modifiers are used to control the visibility of class members.
* Controlling the security level of each individual class and member.

## Default
By default, all class members are private if you do not specify an access modifier.

```csharp
class Car
{
	string model;			// Private
	int year;				// Private
}
```

**Previous:** [Constructors](./04-constructors.md)  
**Next:** [Properties](./06-properties.md)

[Contents](./readme.md)
