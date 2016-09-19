---
title: "Compiler Error CS1655"
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
ms.assetid: 041e9daa-c026-494f-b086-0db9a23c969b
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1655
Cannot pass fields of 'variable' as a ref or out argument because it is a 'readonly variable type'  
  
 This error occurs if you are attempting to pass a member of a [foreach](../Topic/foreach,%20in%20\(C%23%20Reference\).md) variable, a [using](../Topic/using%20Statement%20\(C%23%20Reference\).md) variable, or a [fixed](../vs140/fixed-Statement--C#-Reference-.md) variable to a function as a ref or out argument. Because these variables are considered read-only in these contexts, this is not allowed.  
  
 The following sample generates CS1655:  
  
```  
// CS1655.cs  
struct S   
{  
   public int i;  
}  
  
class CMain  
{  
  static void f(ref int iref)  
  {  
  }  
  
  public static void Main()  
  {  
     S[] sa = new S[10];  
     foreach(S s in sa)  
     {  
        CMain.f(ref s.i);  // CS1655  
     }  
  }  
}  
```