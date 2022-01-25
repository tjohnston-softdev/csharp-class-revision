# Chapter 10 - Interfaces

---

## Definition
* An interface is a completely abstract class.
* Can only contain abstract methods and properties.

## Naming Convention
* It is best practice to start an interface name with an upper-case `I`
* This makes it easy to understand that it is an interface and not a class.
* For example: `IAnimal`

## Example

```csharp
interface IAnimal
{
	void MakeSound();
}

class Cat : IAnimal
{
	public void MakeSound()
	{
		Console.WriteLine("Meow");
	}
}

class Program
{
	static void Main(string[] args)
	{
		Cat myObj = new Cat();
		myObj.MakeSound();
	}
}
```

## Rules
* Similar to abstract classes, you cannot create objects using an interface.
	* eg. You cannot create an `IAnimal` object.
* When implementing an interface, you must override all of its methods.
* An interface can have properties and methods, but not fields.
* Members are `abstract` and `public` by default.
* An interface cannot have a constructor, since it cannot create objects.

## Purpose
* Achieving security by hiding certain details and only showing the important details.
* You cannot inherit from multiple classes, but you can inherit from multiple interfaces.

## Multiple Interfaces

```csharp
// First interface.
interface IFirst
{
	void FirstFunction();
}

// Second interface.
interface ISecond
{
	void SecondFunction();
}

// Inheriting class.
class Demo : IFirst, ISecond
{
	public void FirstFunction()
	{
		Console.WriteLine("First");
	}
	
	public void SecondFunction()
	{
		Console.WriteLine("Second");
	}
}


// Main script.
class Program
{
	static void Main(string[] args)
	{
		Demo myObj = new Demo();
		myObj.FirstFunction();
		myObj.SecondFunction();
	}
}
```

---

**Previous:** [Abstraction](./09-abstraction.md)  
**Next:** [Enumerators](./11-enum.md)

[Contents](./readme.md)
