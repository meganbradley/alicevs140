---
title: "Compiler Error CS1521"
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
ms.assetid: 9a482b33-24f2-4654-81b4-be40bf56d624
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1521
Invalid base type  
  
 A [base](../vs140/base--C#-Reference-.md) class specification was ill formed.  
  
 The following sample generates CS1521:  
  
```  
// CS1521.cs  
class CMyClass  
{  
   public static void Main()  
   {  
   }  
}  
  
class CMyClass1 : CMyClass     // OK  
{  
}  
  
class CMyClass2 : CMyClass[]   // CS1521  
{  
}  
  
class CMyClass3 : CMyClass*    // CS1521  
{  
}  
```