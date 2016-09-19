---
title: "CA1804: Remove unused locals"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-devops-test
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: cc332e67-6543-4813-bd8a-6f6fc75bf22a
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CA1804: Remove unused locals
|||  
|-|-|  
|TypeName|RemoveUnusedLocals|  
|CheckId|CA1804|  
|Category|Microsoft.Performance|  
|Breaking Change|Non-breaking|  
  
## Cause  
 A method declares a local variable but does not use the variable except possibly as the recipient of an assignment statement. For analysis by this rule, the tested assembly must be built with debugging information and the associated program database (.pdb) file must be available.  
  
## Rule Description  
 Unused local variables and unnecessary assignments increase the size of an assembly and decrease performance.  
  
## How to Fix Violations  
 To fix a violation of this rule, remove or use the local variable. Note that the C# compiler that is included with [!INCLUDE[dnprdnlong](../vs140/includes/dnprdnlong_md.md)] removes unused local variables when the `optimize` option is enabled.  
  
## When to Suppress Warnings  
 Suppress a warning from this rule if the variable was compiler emitted. It is also safe to suppress a warning from this rule, or to disable the rule, if performance and code maintenance are not primary concerns.  
  
## Example  
 The following example shows several unused local variables.  
  
 [!CODE [FxCop.Performance.UnusedLocals#1](../CodeSnippet/VS_Snippets_CodeAnalysis/FxCop.Performance.UnusedLocals#1)]  
  
## Related Rules  
 [Avoid excessive locals](../vs140/CA1809--Avoid-excessive-locals.md)  
  
 [Avoid uncalled private code](../Topic/CA1811:%20Avoid%20uncalled%20private%20code.md)  
  
 [Avoid uninstantiated internal classes](../Topic/CA1812:%20Avoid%20uninstantiated%20internal%20classes.md)  
  
 [Avoid unused parameters](../vs140/CA1801--Review-unused-parameters.md)