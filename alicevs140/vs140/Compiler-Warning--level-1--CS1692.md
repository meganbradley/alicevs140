---
title: "Compiler Warning (level 1) CS1692"
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
ms.assetid: 1a6d52e1-0ebb-4990-ac0b-36b05a884a19
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) CS1692
Invalid number  
  
 A number of preprocessor directives, such as `#pragma` and `#line`, use numbers as parameters. One of these numbers is invalid because it is too big, in the wrong format, contains illegal characters, and so on. To correct this error, correct the number.  
  
## Example  
 The following example generates CS1692.  
  
```  
// CS1692.cs  
  
#pragma warning disable a  // CS1692  
// Try this instad:  
// #pragma warning disable 1691  
  
class A  
{  
    static void Main()  
    {  
    }  
}  
```