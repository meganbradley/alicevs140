---
title: "Compiler Error CS1954"
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
ms.assetid: bdec399e-c43d-46d3-a01b-ef3572786fe5
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1954
The best overloaded method match 'method' for the collection initializer element cannot be used. Collection initializer 'Add' methods cannot have ref or out parameters.  
  
 For a collection class to be initialized by using a collection initializer, the class must have a `public``Add` method that is not a `ref` or `out` parameter.  
  
### To correct this error  
  
-   If you can modify the source code of the collection class, provide an `Add` method that does not take a `ref` or `out` parameter.  
  
-   If you cannot modify the collection class, initialize it with the constructors it provides. You cannot use a collection initializer with it.  
  
## Example  
 The following example produces CS1954 because the only available overload of the `Add` list in `MyList` has a `ref` parameter.  
  
```  
// cs1954.cs  
using System.Collections.Generic;  
class MyList<T> : IEnumerable<T>  
{  
    List<T> _list;  
    public void Add(ref T item)  
    {  
        _list.Add(item);  
    }  
  
    public System.Collections.Generic.IEnumerator<T> GetEnumerator()  
    {  
        int index = 0;  
        T current = _list[index];  
        while (current != null)  
        {  
            yield return _list[index++];  
        }  
    }  
  
    System.Collections.IEnumerator System.Collections.IEnumerable.GetEnumerator()  
    {  
        return GetEnumerator();  
    }  
}  
  
public class MyClass  
{  
    public string tree { get; set; }  
}  
class Program  
{  
    static void Main(string[] args)  
    {  
        MyList<MyClass> myList = new MyList<MyClass> { new MyClass { tree = "maple" } }; // CS1954  
    }  
}  
  
```  
  
## See Also  
 [Object and Collection Initializers (C# Programming Guide)](../Topic/Object%20and%20Collection%20Initializers%20\(C%23%20Programming%20Guide\).md)