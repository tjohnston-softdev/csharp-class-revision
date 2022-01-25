# Chapter 02 - Classes and Objects

---

## Definition
* A class is a template for objects.
* An object is an instance of a class.
* When individual objects are created, they inherit all the variables and functions from the class.

## Analogy
* A class is Fruit.
* Objects would be: Apple, Banana, Mango, etc.

## Language
* Everything in C# is associated with classes and objects.
* Classes include attributes and methods.
* For example, a Car is an object. It has:
	* Attributes such as `weight` and `colour`.
	* Methods such as `Drive` and `Brake`
* A class is like an object constructor, or a blueprint for creating objects.

## Creating a Class
* To create a class, use the `class` keyword.
* For example, the Car class has a `colour` attribute.

```csharp
class Car
{
	string colour = "Red";
}
```

## Creating an Object
This snippet creates a `Car` object and prints the `colour` value.

```csharp
class Car
{
	string colour = "Red";
	
	static void Main(string[] args)
	{
		Car myObj = new Car();
		Console.WriteLine(myObj.colour);
	}
}
```

## Using Multiple Objects

```csharp
class Car
{
	string colour = "Red";
	
	static void Main(string[] args)
	{
		Car objectA = new Car();
		Car objectB = new Car();
		
		Console.WriteLine(objectA.colour);
		Console.WriteLine(objectB.colour);
	}
}
```

## Using Multiple Classes
* You can also create an object of a class and access it from within another class.
* This is often used to better organise code:
	* One class has all of the fields and methods.
	* The other class has the `Main()` code, which is the program itself.

**Car File**

```csharp
class Car
{
	public string colour = "Red";
}
```

\
**Program File**

```csharp
class Program
{
	static void Main(string[] args)
	{
		Car myObj = new Car();
		Console.WriteLine(myObj.colour);
	}
}
```


---

**Previous:** [Introduction](./01-introduction.md)  
**Next:** [Class Members](./03-members.md)

[Contents](./readme.md)
