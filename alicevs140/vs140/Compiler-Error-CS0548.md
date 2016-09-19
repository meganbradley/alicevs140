---
title: "Compiler Error CS0548"
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
ms.assetid: c4d34da7-0b4a-4312-ac7f-46db100e43c7
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0548
'property' : property or indexer must have at least one accessor  
  
 A property must have at least one accessor (get or set) method.  
  
 For more information, see and [Using Properties (C# Programming Guide)](../vs140/Using-Properties--C#-Programming-Guide-.md).  
  
## Example  
 The following sample generates CS0548.  
  
```  
// CS0548.cs  
// compile with: /target:library  
public class b  
{  
   public int MyProp {}   // CS0548  
  
   public int MyProp2   // OK  
   {  
      get  
      {  
         return 0;  
      }  
      set {}  
   }  
}  
```