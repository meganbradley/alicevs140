---
title: "How to: Hold More Than One Value in a Variable (Visual Basic)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5fe0e558-aac2-4a40-b7f2-7cfea7336917
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Hold More Than One Value in a Variable (Visual Basic)
A variable holds more than one value if you declare it to be of a *composite data type*.  
  
 [Composite Data Types](../vs140/Composite-Data-Types--Visual-Basic-.md) include structures, arrays, and classes. A variable of a composite data type can hold a combination of elementary data types and other composite types. Structures and classes can hold code as well as data.  
  
### To hold more than one value in a variable  
  
1.  Determine what composite data type you want to use for your variable.  
  
2.  If the composite data type is not already defined, define it so that your variable can use it.  
  
    -   Define a structure with a [Structure Statement](../Topic/Structure%20Statement.md).  
  
    -   Define an array with a [Dim Statement (Visual Basic)](../Topic/Dim%20Statement%20\(Visual%20Basic\).md).  
  
    -   Define a class with a [Class Statement (Visual Basic)](../Topic/Class%20Statement%20\(Visual%20Basic\).md).  
  
3.  Declare your variable with a `Dim` statement.  
  
4.  Follow the variable name with an `As` clause.  
  
5.  Follow the `As` keyword with the name of the appropriate composite data type.  
  
## See Also  
 [Data Type Summary (Visual Basic)](../Topic/Data%20Type%20Summary%20\(Visual%20Basic\).md)   
 [Type Characters](../vs140/Type-Characters--Visual-Basic-.md)   
 [Composite Data Types](../vs140/Composite-Data-Types--Visual-Basic-.md)   
 [Structures](../vs140/Structures--Visual-Basic-.md)   
 [Arrays](../Topic/Arrays%20in%20Visual%20Basic.md)   
 [Objects and Classes in Visual Basic](../Topic/Objects%20and%20Classes%20in%20Visual%20Basic.md)   
 [Value Types and Reference Types](../Topic/Value%20Types%20and%20Reference%20Types.md)