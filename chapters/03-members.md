# Chapter 03 - Class Members

---

## Definition
* Fields and methods that are inside classes.
* For example, this class has two fields and one method.

```csharp
// Class
class Car
{
	// Fields
	string colour = "Red";
	int maxSpeed = 200;
	
	// Method
	public void FullThrottle()
	{
		Console.WriteLine("Full Throttle");
	}
}
```

## Field Values
This snippet creates a Car object and prints the field values.

```csharp
class Car
{
	string colour = "Red";
	int maxSpeed = 200;
	
	static void Main(string[] args)
	{
		Car myObj = new Car();
		Console.WriteLine(myObj.colour);
		Console.WriteLine(myObj.maxSpeed);
	}
}
```

## Blank Fields
* You can also leave fields blank and modify them when creating an individual object.
* This is useful when creating multiple objects of one class.

```csharp
class Car
{
	string model;
	string colour;
	int year;
	
	static void Main(string[] args)
	{
		Car ford = new Car();
		ford.model = "Mustang";
		ford.colour = "Red";
		ford.year = 1969;
		
		Car opel = new Car();
		opel.model = "Astra";
		opel.colour = "White";
		opel.year = 2005;
		
		Console.WriteLine(ford.model);
		Console.WriteLine(opel.model);
	}
}
```

## Methods

```csharp
class Car
{
	string model;
	string colour;
	int maxSpeed;
	int year;
	
	public void FullThrottle()
	{
		Console.WriteLine("Full Throttle");
	}
	
	static void Main(string[] args)
	{
		Car myObj = new Car();
		myObj.FullThrottle();
	}
}
```

## Multiple Classes

**Car File**

```csharp
class Car
{
	string model;
	string colour;
	int maxSpeed;
	int year;
	
	public void FullThrottle()
	{
		Console.WriteLine("Full Throttle");
	}
}
```

\
**Program File**

```csharp
class Program
{
	static void Main(string[] args)
	{
		Car ford = new Car();
		ford.model = "Mustang";
		ford.colour = "Red";
		ford.maxSpeed = 250;
		ford.year = 1969;
		
		Car opel = new Car();
		opel.model = "Astra";
		opel.colour = "White";
		opel.maxSpeed = 175;
		opel.year = 2005;
		
		Console.WriteLine(ford.model);
		Console.WriteLine(opel.model);
	}
}
```

---

**Previous:** [Classes and Objects](./02-classes_objects.md)  
**Next:** [Constructors](./04-constructors.md)

[Contents](./readme.md)
