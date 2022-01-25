# Chapter 09 - Abstraction

---

## Definition
* Data abstraction is the process of hiding certain details and only showing essential information to the user.
* This can be achieved using abstract classes or interfaces.

## Keyword
* The `abstract` keyword can be used for classes or methods.
* An abstract class cannot be used to create objects. It must be inherited.
* An abstract method:
	* Can only be used in an abstract class.
	* Does not have a body. It is set in a derived class after being inherited.

## Syntax

```csharp
abstract class Animal
{
	public abstract void MakeSound();
	
	public void Sleep()
	{
		Console.WriteLine("ZzZ");
	}
}
```

## Abstract Objects
* It is not possible to create objects from an abstract class.
* If you attempt to do this, there will be an error.
* To access the abstract class, it must be inherited from another class.

```
Cannot create an instance of the abstract class or interface 'Animal'
```

## Example

```csharp
abstract class Animal
{
	public abstract void MakeSound();
	
	public void Sleep()
	{
		Console.WriteLine("ZzZ");
	}
}

class Dog : Animal
{
	public override void MakeSound()
	{
		Console.WriteLine("Woof");
	}
}

class Program
{
	static void Main(string[] args)
	{
		Dog myObj = new Dog();
		myObj.MakeSound();
		myObj.Sleep();
	}
}
```

---

**Previous:** [Polymorphism](./08-polymorphism.md)  
**Next:** [Interfaces](./10-interfaces.md)

[Contents](./readme.md)
