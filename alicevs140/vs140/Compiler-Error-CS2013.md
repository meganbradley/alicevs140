---
title: "Compiler Error CS2013"
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
ms.assetid: 8a57b4c8-02fc-4f73-b489-121ff468c17d
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS2013
Invalid image base number 'value'  
  
 An invalid value (not a number) was passed to the [/baseaddress](../Topic/-baseaddress%20\(C%23%20Compiler%20Options\).md) compiler option.  
  
 The following sample generates CS2013:  
  
```  
// CS2013.cs  
// compile with: /target:library /baseaddress:x  
// CS2013 expected  
class MyClass  
{  
}  
```