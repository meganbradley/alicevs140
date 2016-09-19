---
title: "Compiler Error CS1679"
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
ms.assetid: c42e9bca-212a-458e-88f8-b81c812436bb
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1679
Invalid extern alias for '/reference'; 'identifier' is not a valid identifier  
  
 When using the external assembly alias feature of the **/reference** option, the text that follows **/reference:** and that precedes the '=' must be a valid C# identifier or keyword according to the C# Language Specification.  
  
 To correct this error, change text before the "=" to a valid C# identifier or keyword.  
  
## Example  
 The following example generates CS1679.  
  
```  
// CS1679.cs  
// compile with: /reference:123$BadIdentifier%=System.dll  
class TestClass {  
    static void Main()  
    {  
    }  
}  
```