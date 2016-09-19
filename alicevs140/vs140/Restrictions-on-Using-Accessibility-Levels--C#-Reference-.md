---
title: "Restrictions on Using Accessibility Levels (C# Reference)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 987e2f22-46bf-4fea-80ee-270b9cd01045
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Restrictions on Using Accessibility Levels (C# Reference)
When you specify a type in a declaration, check whether the accessibility level of the type is dependent on the accessibility level of a member or of another type. For example, the direct base class must be at least as accessible as the derived class. The following declarations cause a compiler error because the base class `BaseClass` is less accessible than `MyClass`:  
  
```  
class BaseClass {...}  
public class MyClass: BaseClass {...} // Error  
```  
  
 The following table summarizes the restrictions on declared accessibility levels.  
  
|Context|Remarks|  
|-------------|-------------|  
|[Classes](../vs140/Classes--C#-Programming-Guide-.md)|The direct base class of a class type must be at least as accessible as the class type itself.|  
|[Interfaces](../Topic/Interfaces%20\(C%23%20Programming%20Guide\).md)|The explicit base interfaces of an interface type must be at least as accessible as the interface type itself.|  
|[Delegates](../Topic/Delegates%20\(C%23%20Programming%20Guide\).md)|The return type and parameter types of a delegate type must be at least as accessible as the delegate type itself.|  
|[Constants](../Topic/Constants%20\(C%23%20Programming%20Guide\).md)|The type of a constant must be at least as accessible as the constant itself.|  
|[Fields](../vs140/Fields--C#-Programming-Guide-.md)|The type of a field must be at least as accessible as the field itself.|  
|[Methods](../Topic/Methods%20\(C%23%20Programming%20Guide\).md)|The return type and parameter types of a method must be at least as accessible as the method itself.|  
|[Properties](../vs140/Properties--C#-Programming-Guide-.md)|The type of a property must be at least as accessible as the property itself.|  
|[Events](../Topic/Events%20\(C%23%20Programming%20Guide\).md)|The type of an event must be at least as accessible as the event itself.|  
|[Indexers](../vs140/Indexers--C#-Programming-Guide-.md)|The type and parameter types of an indexer must be at least as accessible as the indexer itself.|  
|[Operators](../Topic/Operators%20\(C%23%20Programming%20Guide\).md)|The return type and parameter types of an operator must be at least as accessible as the operator itself.|  
|[Constructors](../vs140/Constructors--C#-Programming-Guide-.md)|The parameter types of a constructor must be at least as accessible as the constructor itself.|  
  
## Example  
 The following example contains erroneous declarations of different types. The comment following each declaration indicates the expected compiler error.  
  
```  
// Restrictions on Using Accessibility Levels  
// CS0052 expected as well as CS0053, CS0056, and CS0057  
// To make the program work, change access level of both class B  
// and MyPrivateMethod() to public.  
  
using System;  
  
// A delegate:  
delegate int MyDelegate();  
  
class B  
{  
    // A private method:  
    static int MyPrivateMethod()  
    {  
        return 0;  
    }  
}  
  
public class A  
{  
    // Error: The type B is less accessible than the field A.myField.  
    public B myField = new B();  
  
    // Error: The type B is less accessible  
    // than the constant A.myConst.  
    public readonly B myConst = new B();  
  
    public B MyMethod()  
    {  
        // Error: The type B is less accessible   
        // than the method A.MyMethod.  
        return new B();  
    }  
  
    // Error: The type B is less accessible than the property A.MyProp  
    public B MyProp  
    {  
        set  
        {  
        }  
    }  
  
    MyDelegate d = new MyDelegate(B.MyPrivateMethod);  
    // Even when B is declared public, you still get the error:   
    // "The parameter B.MyPrivateMethod is not accessible due to   
    // protection level."  
  
    public static B operator +(A m1, B m2)  
    {  
        // Error: The type B is less accessible  
        // than the operator A.operator +(A,B)  
        return new B();  
    }  
  
    static void Main()  
    {  
        Console.Write("Compiled successfully");  
    }  
}  
```  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [C# Keywords](../Topic/C%23%20Keywords.md)   
 [Access Modifiers](../vs140/Access-Modifiers--C#-Reference-.md)   
 [Accessibility Domain](../vs140/Accessibility-Domain--C#-Reference-.md)   
 [Accessibility Levels](../vs140/Accessibility-Levels--C#-Reference-.md)   
 [Access Modifiers (Visual C#)](../Topic/Access%20Modifiers%20\(C%23%20Programming%20Guide\).md)   
 [public (C# Programmer's Reference)](../vs140/public--C#-Reference-.md)   
 [private (C# Programmer's Reference)](../vs140/private--C#-Reference-.md)   
 [protected (C# Programmer's Reference)](../vs140/protected--C#-Reference-.md)   
 [internal (C# Programmer's Reference)](../vs140/internal--C#-Reference-.md)