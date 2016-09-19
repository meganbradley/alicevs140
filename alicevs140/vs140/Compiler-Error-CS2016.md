---
title: "Compiler Error CS2016"
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
ms.assetid: 69f77502-f726-4856-ac87-e556eeb67349
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS2016
Code page 'codepage' is invalid or not installed  
  
 The [/codepage](../vs140/-codepage--C#-Compiler-Options-.md) compiler option was passed an invalid value.  
  
 The following sample generates CS2016:  
  
```  
// CS2016.cs  
// compile with: /codepage:x  
// CS2016 expected  
class MyClass  
{  
   public static void Main()  
   {  
   }  
}  
```