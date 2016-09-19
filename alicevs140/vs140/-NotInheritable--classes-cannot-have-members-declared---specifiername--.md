---
title: "&#39;NotInheritable&#39; classes cannot have members declared &#39;&lt;specifiername&gt;&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c800e24e-d055-402f-b378-6d2f4041ff16
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;NotInheritable&#39; classes cannot have members declared &#39;&lt;specifiername&gt;&#39;
Override modifiers cannot be used with `NotInheritable` classes because their members cannot be overridden.  
  
 **Error ID:** BC30607  
  
### To correct this error  
  
-   Remove override modifiers, such as `Overridable`, `NotOverridable`, or `MustOverride`, from the class definition.  
  
## See Also  
 [Overridable](../vs140/Overridable--Visual-Basic-.md)   
 [NotOverridable](../vs140/NotOverridable--Visual-Basic-.md)   
 [MustOverride](../vs140/MustOverride--Visual-Basic-.md)   
 [NOT IN BUILD: Overriding Properties and Methods](assetId:///2167e8f5-1225-4b13-9ebd-02591ba90213)