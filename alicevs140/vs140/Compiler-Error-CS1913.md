---
title: "Compiler Error CS1913"
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
ms.assetid: 652494b3-9576-4a4c-a9ee-695f86c4a023
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1913
Member 'name' cannot be initialized. It is not a field or property.  
  
 Object initializers can only be used to initialize accessible fields or properties.  
  
### To correct this error  
  
1.  Initialize the class member in a regular constructor or other initialization method.  
  
## Example  
 The following example generates CS1913:  
  
```  
// cs1912.cs  
class A  
{  
    public delegate void D();  
    public event D myEvent;  
}  
  
public class Test  
{  
    static void Main()  
    {  
  
        A a = new A() {myEvent = M}; // CS1913  
    }  
  
    public void M(){}  
}  
```  
  
## See Also  
 [Objects, Classes and Structs (C# Programming Guide)](../Topic/Classes%20and%20Structs%20\(C%23%20Programming%20Guide\).md)