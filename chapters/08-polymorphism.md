# Chapter 08 - Polymorphism

---

## Definition
* Polymorphism means "many forms"
* It occurs when we have many classes that relate to each other by inheritance.
* If we can inherit fields and methods from other classes, polymorphism uses those methods to perform different tasks.
* This allows us to perform a single action in different ways.

## Analogy
* Consider a base class 'Animal' with the method `MakeSound`
* Derived classes can be Pigs, Cats, Dogs, Birds, etc.
* Each animal makes a different sound so each class would have its own implementation of `MakeSound`

## Example

\
**Code**

```csharp
class Animal
{
	public virtual void MakeSound()
	{
		Console.WriteLine("The Animal makes a sound.");
	}
}

class Dog : Animal
{
	public override void MakeSound()
	{
		Console.WriteLine("Woof");
	}
}

class Cat : Animal
{
	public override void MakeSound()
	{
		Console.WriteLine("Meow");
	}
}

class Program
{
	static void Main(string[] args)
	{
		Animal animalObj = new Animal();
		Dog dogObj = new Dog();
		Cat catObj = new Cat();
		
		animalObj.MakeSound();
		dogObj.MakeSound();
		catObj.MakeSound();
	}
}
```

\
**Output**

```
The Animal makes a sound.
Woof
Meow
```

---

**Previous:** [Inheritance](./07-inheritance.md)  
**Next:** [Abstraction](./09-abstraction.md)

[Contents](./readme.md)
