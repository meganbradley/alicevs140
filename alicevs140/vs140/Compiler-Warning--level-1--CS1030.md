---
title: "Compiler Warning (level 1) CS1030"
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
ms.assetid: 7c565abc-1366-4641-9383-ab8ba026ab96
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) CS1030
\#warning: 'text'  
  
 Displays the text of a warning defined with the [#warning](../vs140/#warning--C#-Reference-.md) directive.  
  
 The following sample shows how to create a user-defined warning:  
  
```  
// CS1030.cs  
class Sample  
{  
   static void Main()  
   {  
      #warning Let's give a warning here   // CS1030  
   }  
}  
```