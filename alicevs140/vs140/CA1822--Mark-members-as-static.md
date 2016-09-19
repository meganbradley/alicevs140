---
title: "CA1822: Mark members as static"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-devops-test
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 743f0af7-41d1-4852-8d97-af0688b31118
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CA1822: Mark members as static
|||  
|-|-|  
|TypeName|MarkMembersAsStatic|  
|CheckId|CA1822|  
|Category|Microsoft.Performance|  
|Breaking Change|Non-breaking - If the member is not visible outside the assembly, regardless of the change you make. Non Breaking - If you just change the member to an instance member with the `this` keyword.<br /><br /> Breaking - If you change the member from an instance member to a static member and it is visible outside the assembly.|  
  
## Cause  
 A member that does not access instance data is not marked as static (Shared in [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)]).  
  
## Rule Description  
 Members that do not access instance data or call instance methods can be marked as static (Shared in [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)]). After you mark the methods as static, the compiler will emit nonvirtual call sites to these members. Emitting nonvirtual call sites will prevent a check at runtime for each call that makes sure that the current object pointer is non-null. This can achieve a measurable performance gain for performance-sensitive code. In some cases, the failure to access the current object instance represents a correctness issue.  
  
## How to Fix Violations  
 Mark the member as static (or Shared in [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)]) or use 'this'/'Me' in the method body, if appropriate.  
  
## When to Suppress Warnings  
 It is safe to suppress a warning from this rule for previously shipped code for which the fix would be a breaking change.  
  
## Related Rules  
 [Avoid uncalled private code](../Topic/CA1811:%20Avoid%20uncalled%20private%20code.md)  
  
 [Avoid uninstantiated internal classes](../Topic/CA1812:%20Avoid%20uninstantiated%20internal%20classes.md)  
  
 [Remove unused locals](../vs140/CA1804--Remove-unused-locals.md)