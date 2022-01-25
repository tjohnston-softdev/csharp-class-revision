# Chapter 04 - Constructors

---

## Definition
* Special method used to initialise objects.
* The advantage is that it is called when a class object is created.
* Can be used to set initial values for fields.

## Rules
* The constructor name must match the class name.
* Cannot have a return type.

## Overloading
Just like other methods, constructors can be overloaded using different combinations of parameters.

## Example

```csharp
class Car
{
	string model;
	string colour;
	int year;
	
	public Car(string pModel, string pColour, int pYear)
	{
		model = pModel;
		colour = pColour;
		year = pYear;
	}
	
	public void Display()
	{
		string prepTxt = "";
		
		prepTxt += colour;
		prepTxt += " ";
		prepTxt += year.ToString();
		prepTxt += " ";
		prepTxt += model;
		
		Console.WriteLine(prepTxt);
	}
	
	
	static void Main(string[] args)
	{
		Car myObj = new Car("Mustang", "Red", 1969);
		myObj.Display();
	}
}
```

## Saving Time
Constructors are very useful in reducing the amount of code.

\
**Before**

```csharp
using System;

namespace MyApplication
{
  class Program
  {
    static void Main(string[] args)
    {
      Car Ford = new Car();
      Ford.model = "Mustang";
      Ford.color = "red";
      Ford.year = 1969;

      Car Opel = new Car();
      Opel.model = "Astra";
      Opel.color = "white";
      Opel.year = 2005;

      Console.WriteLine(Ford.model);
      Console.WriteLine(Opel.model);
    }
  }
}
```

\
**After**

```csharp
using System;

namespace MyApplication
{
  class Program
  {
    static void Main(string[] args)
    {
      Car Ford = new Car("Mustang", "Red", 1969);
      Car Opel = new Car("Astra", "White", 2005);

      Console.WriteLine(Ford.model);
      Console.WriteLine(Opel.model);
    }
  }
}
```

---

**Previous:** [Class Members](./03-members.md)  
**Next:** [Access Modifiers](./05-access.md)

[Contents](./readme.md)
