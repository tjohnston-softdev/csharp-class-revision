# Chapter 06 - Properties

---

## Encapsulation Definition
* Making sure that sensitive data is hidden from the users.
* To do this, you must:
	* Declare fields and variables as private.
	* Provide public `get` and `set` methods through properties.

## Encapsulation Benefits
* Better control of class members.
* Reducing the number of possible ways to mess up the code.
* Fields can be made read or write only, depending on methods used.
* You can change one part of the code without affecting the others.
* Increased data security.

## Property
* Basically a combination between a variable and a method.
* Has two methods: `get` and `set`

## Example

```csharp
class Person
{
	private string pName;
	
	public string Name
	{
		get {return pName;}
		set {pName = value;}
	}
}

class Program
{
	static void Main(string[] args)
	{
		Person myObj = new Person();
		myObj.Name = "John";
		Console.WriteLine(myObj.Name);
	}
}
```

## Explanation
* The `Name` property is associated with the `pName` field.
* The `get` method returns `pName`
* The `set` method assigns a value to `pName`
* The `value` keyword represents the value that we are assigning to the property.
* Now we can use the `Name` property to access the private field.

## Automatic Properties
* C# provides a way to use short-hand or automatic properties.
* You do not have to define the field for the property.
* You only have to write `get;` and `set;` inside the property.
* This example produces the same result as above but with less code.

```csharp
class Person
{
	public string Name
	{get; set;}
}

class Program
{
	static void Main(string[] args)
	{
		Person myObj = new Person();
		myObj.Name = "John";
		Console.WriteLine(myObj.Name);
	}
}
```

---

**Previous:** [Access Modifiers](./05-access.md)  
**Next:** [Inheritance](./07-inheritance.md)

[Contents](./readme.md)
