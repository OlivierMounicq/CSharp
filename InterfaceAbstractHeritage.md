The class B and C have to implement the method ApplyMethod(). But for some classes, we want to share the same method behavior.  

```cs

public interface I
{
  string ApplyMethod();
}

public abstract class A
{
  //This method has to be public (not protected)
  public virtual string ApplyMethod()
  {
    return "Base abstract class A";
  }
}

public class B: A, I
{
  public override string ApplyMethod()
  {
    return "Base abstract class B";
  }
}

public class C: A, I
{
}

var b = new B();
Console.WriteLine(b.ApplyMethod());

var c = new C();
Console.WriteLine(c.ApplyMethod());

//Output
//Base abstract class B
//Base abstract class A

```




