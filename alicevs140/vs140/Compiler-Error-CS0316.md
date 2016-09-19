---
title: "Compiler Error CS0316"
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
ms.assetid: 8b70abbe-dd4f-473f-8dfe-f8309abef276
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0316
The parameter name 'name' conflicts with an automatically-generated parameter name.  
  
 Reserved words cannot be used as parameter names. In the example that follows, `value` is a reserved word in the context of a default property or indexer accessor.  
  
### To correct this error  
  
1.  Change the name of the parameter.  
  
## Example  
 The following code generates CS0316:  
  
```  
// cs0316.cs  
// Compile with: /target:library  
public class Test  
{  
    public int this[int value] // CS0316  
    {  
        get { return 1; }  
        set { }  
    }  
}  
```  
  
## See Also  
 [Indexers (C# Programming Guide)](../vs140/Indexers--C#-Programming-Guide-.md)   
 [C# Keywords](../Topic/C%23%20Keywords.md)