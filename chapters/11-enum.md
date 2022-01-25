# Chapter 11 - Enumeration

---

## Definition
* An `enum` is a special class that represents a group of constants.
* It is basically the same thing as a drop-down list.
* `enum` is short for 'enumerations' which means "specifically listed"

## Syntax

```csharp
enum Level
{
	LOW,
	MEDIUM,
	HIGH
}

class Program
{
	static void Main(string[] args)
	{
		Level chosenOpt = Level.MEDIUM;
		Console.WriteLine(chosenOpt);
	}
}
```

## Class
You can include `enum` objects inside a class.

```csharp
class Program
{
	enum Level
	{
		LOW,
		MEDIUM,
		HIGH
	}
	
	static void Main(string[] args)
	{
		Level chosenOpt = Level.LOW;
		Console.WriteLine(chosenOpt);
	}
}
```

## Usage
* You should use `enum` objects when you have values that you know are not going to change.
* In other words, they are constant.
* Months, days of the week, colours, etc.

---

**Previous:** [Interfaces](./10-interfaces.md)  
**Next:**

[Contents](./readme.md)
