---
title: "Default property &#39;&lt;propertyname1&gt;&#39; conflicts with default property &#39;&lt;propertyname2&gt;&#39; in &#39;&lt;classname&gt;&#39; and so should be declared &#39;Shadows&#39;"
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
ms.assetid: 692ccf76-5715-4f11-a972-84cf9de30bc1
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Default property &#39;&lt;propertyname1&gt;&#39; conflicts with default property &#39;&lt;propertyname2&gt;&#39; in &#39;&lt;classname&gt;&#39; and so should be declared &#39;Shadows&#39;
A property is declared with the same name as a property defined in the base class. In this situation, the property in this class should shadow the base class property.  
  
 This message is a warning. `Shadows` is assumed by default. For more information about hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](../vs140/Configuring-Warnings-in-Visual-Basic.md).  
  
 **Error ID:** BC40007  
  
### To correct this error  
  
-   Add the `Shadows` keyword to the declaration, or change the name of the property being declared.  
  
## See Also  
 [Shadows](../vs140/Shadows--Visual-Basic-.md)   
 [Shadowing in Visual Basic](../vs140/Shadowing-in-Visual-Basic.md)