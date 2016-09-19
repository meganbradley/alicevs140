---
title: "Member &#39;&lt;membername&gt;&#39; conflicts with member &#39;&lt;membername&gt;&#39; in the base type &#39;&lt;basetypename&gt;&#39; and so should not be declared &#39;Overloads&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2ec72726-ab0e-4545-9c1e-2409eb54482e
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Member &#39;&lt;membername&gt;&#39; conflicts with member &#39;&lt;membername&gt;&#39; in the base type &#39;&lt;basetypename&gt;&#39; and so should not be declared &#39;Overloads&#39;
A property or procedure uses the [Overloads](../vs140/Overloads--Visual-Basic-.md) keyword to redeclare an existing property or procedure with the same name, but the existing property or procedure is in the base class.  
  
 Overloading is used to define multiple versions of a property or procedure all in the same class. You cannot define an additional version of a base class member unless the base class member already specifies [Overloads](../vs140/Overloads--Visual-Basic-.md).  
  
 By default, this message is a warning. For more information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](../vs140/Configuring-Warnings-in-Visual-Basic.md).  
  
 **Error ID:** BC40021  
  
### To correct this error  
  
-   If you intend to define an additional version of the base class member and have access to the source code of the base class, add the [Overloads](../vs140/Overloads--Visual-Basic-.md) keyword to the base class definition.  
  
-   If you do not have access to the source code of the base class, you cannot overload the member in a derived class. Remove the `Overloads` keyword.  
  
-   If you wish to replace the base class member instead of defining an additional version of it, use the [Overrides](../vs140/Overrides--Visual-Basic-.md) keyword instead of `Overloads`.  
  
-   If you wish to hide the base class member with a new member in the derived class, use the [Shadows](../vs140/Shadows--Visual-Basic-.md) keyword instead of `Overloads`.  
  
## See Also  
 [Procedure Overloading](../Topic/Procedure%20Overloading%20\(Visual%20Basic\).md)   
 [Inheritance Basics](../vs140/Inheritance-Basics--Visual-Basic-.md)