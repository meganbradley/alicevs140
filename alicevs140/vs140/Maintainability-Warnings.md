---
title: "Maintainability Warnings"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-devops-test
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 537e70ca-a88c-49df-bfc7-0ee63bbe4f16
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Maintainability Warnings
Maintainability warnings support library and application maintenance.  
  
## In This Section  
  
|Rule|Description|  
|----------|-----------------|  
|[CA1500: Variable names should not match field names](../vs140/CA1500--Variable-names-should-not-match-field-names.md)|An instance method declares a parameter or a local variable whose name matches an instance field of the declaring type, which leads to errors.|  
|[CA1501: Avoid excessive inheritance](../vs140/CA1501--Avoid-excessive-inheritance.md)|A type is more than four levels deep in its inheritance hierarchy. Deeply nested type hierarchies can be difficult to follow, understand, and maintain.|  
|[CA1502: Avoid excessive complexity](../vs140/CA1502--Avoid-excessive-complexity.md)|This rule measures the number of linearly independent paths through the method, which is determined by the number and complexity of conditional branches.|  
|[CA1504: Review misleading field names](../vs140/CA1504--Review-misleading-field-names.md)|The name of an instance field starts with "s_", or the name of a static (Shared in [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)]) field starts with "m_".|  
|[CA1505: Avoid unmaintainable code](../vs140/CA1505--Avoid-unmaintainable-code.md)|A type or method has a low maintainability index value. A low maintainability index indicates that a type or method is probably difficult to maintain and would be a good candidate for redesign.|  
|[CA1506: Avoid excessive class coupling](../vs140/CA1506--Avoid-excessive-class-coupling.md)|This rule measures class coupling by counting the number of unique type references that a type or method contains.|  
  
## See Also  
 [Measuring Complexity and Maintainability of Managed Code](../vs140/Measuring-Complexity-and-Maintainability-of-Managed-Code.md)