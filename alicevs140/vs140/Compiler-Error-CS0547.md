---
title: "Compiler Error CS0547"
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
ms.assetid: aa80873f-deb0-4ff2-8435-92a626bb5b80
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0547
'property' : property or indexer cannot have void type  
  
 [void](../vs140/void--C#-Reference-.md) is invalid as a return value for a property.  
  
 For more information, see [Properties](../vs140/Properties--C#-Programming-Guide-.md).  
  
 The following sample generates CS0547:  
  
```  
// CS0547.cs  
public class a  
{  
   public void i   // CS0547  
   // Try the following declaration instead:  
   // public int i  
   {  
      get  
      {  
         return 0;  
      }  
   }  
}  
  
public class b : a  
{  
   public static void Main()  
   {  
   }  
}  
```