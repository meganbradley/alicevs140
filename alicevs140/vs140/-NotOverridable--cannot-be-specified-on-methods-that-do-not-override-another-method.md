---
title: "&#39;NotOverridable&#39; cannot be specified on methods that do not override another method"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0241197c-51fa-48b8-9a2a-4205d25641d3
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;NotOverridable&#39; cannot be specified on methods that do not override another method
Properties and methods are `NotOverridable` by default. The `NotOverridable` modifier can only be used on methods that override another property or method.  
  
 **Error ID:** BC31088  
  
### To correct this error  
  
-   Remove the `NotOverridable` modifier from properties and methods that do not override another member.  
  
## See Also  
 [Overrides](../vs140/Overrides--Visual-Basic-.md)   
 [Overloads](../vs140/Overloads--Visual-Basic-.md)   
 [NotOverridable](../vs140/NotOverridable--Visual-Basic-.md)   
 [Overridable](../vs140/Overridable--Visual-Basic-.md)