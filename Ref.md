

```cs
public class Program
{
  public static void Main(string[] args)
  {
    var person = new Person("Albert", "Einstein");
    Console.WriteLine(person);
    
    UpdateOne(person);
    Console.WriteLine(person);
    
    UpdateTwo(person);
    Console.WriteLine(person);
  }

  public static void UpdateOne(Person person)
  {
    person = new Person("Richard", "Feynmann");
    Console.WriteLine(person);
  }
  
  public static void UpdateTwo(ref Person person)
  {
    person = new Person("Richard", "Feynmann");
    Console.WriteLine(person);
  }  

}

public class Person
{
  public string FirstName {get;}
  
  public string LastName {get;}
  
  public Person(string firstName, string lastName)
  {
    FirstName = firstName;
    LastName = lastName;
  }
  
  public override string ToString()
  {
    return $"{FirstName} {Lastname}";
  }
}




``` 

Result :

Albert Einstein  
Richard Feynmann  
Albert Einstein  
Richard Feynmann  
Richard Feynmann


