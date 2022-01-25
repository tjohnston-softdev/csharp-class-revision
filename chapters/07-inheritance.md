# Chapter 07 - Inheritance

---

## Definition
* It is possible for child classes to inherit fields and methods from a parent class.
* The derived class inherits from the base.
* The base class is being inherited by the derived.

## Syntax
To inherit from a class, use the `:` symbol.

```csharp
class Vehicle					// Parent
class Car : Vehicle				// Child
```

## Usage
* The good thing about inheritance is that it enables code re-usability.
* Re-using fields and methods from an existing class when creating a new class.

## Example

```csharp
// Base class.
class Vehicle
{
	public string brand = "Ford";
	
	public void Honk()
	{
		Console.WriteLine("Beep Beep");
	}
}


// Derived class
class Car : Vehicle
{
	public string model = "Mustang";
}


// Main script
class Program
{
	static void Main(string[] args)
	{
		Car myObj = new Car();
		myObj.Honk();
		Console.WriteLine(myObj.brand + " " + myObj.model);
	}
}
```

## Sealed Class
* If you don't want other classes to inherit from a particular class, use the `sealed` keyword.
* If you try to access a `sealed` class, there will be an error.

\
**Code**

```csharp
sealed class Vehicle
{
	// You cannot inherit from this class.
}

class Car : Vehicle
{
	// There will be an error.
}
```

\
**Error**

```
'Car': cannot derive from sealed type 'Vehicle'
```

---

**Previous:** [Properties](./06-properties.md)  
**Next:** [Polymorphism](./08-polymorphism.md)

[Contents](./readme.md)
