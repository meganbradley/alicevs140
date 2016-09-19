---
title: "Compiler Error CS0738"
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
ms.assetid: 01ce94ee-2435-4326-befc-2b020c441a4f
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0738
'type name' does not implement interface member 'member name'. 'method name' cannot implement 'interface member' because it does not have the matching return type of ' type name'.  
  
 The return value of an implementing method in a class must match the return value of the interface member that it implements.  
  
### To correct this error  
  
1.  Change the return type of the method to match that of the interface member.  
  
## Example  
 The following code generates CS0738 because the class method returns `void` and the interface member of the same name returns `int`:  
  
```  
using System;  
  
interface ITest  
{  
    int TestMethod();  
}  
public class Test: ITest  
{  
    public void TestMethod() { } // CS0738  
    // Try the following line instead.  
    // public int TestMethod();  
}  
```  
  
## See Also  
 [Interfaces (C# Programming Guide)](../Topic/Interfaces%20\(C%23%20Programming%20Guide\).md)