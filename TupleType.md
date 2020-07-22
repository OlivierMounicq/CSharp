Tuple Type C 7.0


```cs
using System.Collection.Generic;
using System.Linq;

namespace TupleType
{
  public class Program
  {
    public static void Main(string[] args)
    {
      var list = new List<(int Id, string FirstName, string LastName)>();
      list.Add((Id : 1, FirstName : "Albert", LastName : "Einstein"));
      list.Add((Id : 2, FirstName : "Richard", LastName : "Feynmann"));
      
      var res = list.FirstOrDefault(r => r.FirstName = "Marie" && r.LastName = "Curie");
      var id = res.Id; //0
      var firstName = res.FirstName; //null
      
      //If we use First method, an exception is thrown
      var tmp = list.First(r => r.FirstName = "Marie" && r.LastName = "Curie");      
    }
  }
}
```
