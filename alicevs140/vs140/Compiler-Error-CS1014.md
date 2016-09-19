---
title: "Compiler Error CS1014"
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
ms.assetid: 60c1e9af-5a0d-4ae0-a2e6-881b0d1535e9
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1014
A get or set accessor expected  
  
 A method declaration was found in a property declaration. You can only declare `get` and `set` methods in a property.  
  
 For more information on properties, see [Using Properties](../vs140/Using-Properties--C#-Programming-Guide-.md).  
  
## Example  
 The following sample generates CS1014.  
  
```  
// CS1014.cs  
// compile with: /target:library  
class Sample  
{  
   public int TestProperty  
   {  
      get  
      {  
         return 0;  
      }  
      int z;   // CS1014  not get or set  
   }  
}  
```