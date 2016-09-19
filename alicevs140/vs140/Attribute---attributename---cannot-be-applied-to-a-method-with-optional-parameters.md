---
title: "Attribute &#39;&lt;attributename&gt;&#39; cannot be applied to a method with optional parameters"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4de3d2c9-5588-47c2-a6b2-e165d16106b8
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Attribute &#39;&lt;attributename&gt;&#39; cannot be applied to a method with optional parameters
The attribute can only be used with methods that use required arguments or no arguments.  
  
 **Error ID:** BC30645  
  
### To correct this error  
  
1.  Define the method without optional parameters.  
  
2.  Use an attribute that can be used with methods that have optional parameters.  
  
3.  Define a custom attribute that can be used in this context.  
  
## See Also  
 <xref:System.AttributeUsageAttribute?qualifyHint=False>   
 [NOT IN BUILD: Attributes in Visual Basic](assetId:///620bfc0e-4582-4c8b-8432-ebc5c3dccc22)