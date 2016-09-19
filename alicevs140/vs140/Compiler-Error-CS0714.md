---
title: "Compiler Error CS0714"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fbb5dc55-645c-4980-bf4b-3c2f84a3c6cd
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0714
'static type' : static classes cannot implement interfaces  
  
 Interfaces may define non-static methods on objects and hence may not be implemented by static classes. To resolve this error, make sure your class does not attempt to implement any interfaces.  
  
## Example  
 The following sample generates CS0714:  
  
```  
// CS0714.cs  
interface I  
{  
}  
  
public static class C : I  // CS0714  
{  
    public static void Main()  
    {  
    }  
}  
```