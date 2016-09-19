---
title: "MSBuild Conditions"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
  - CSharp
  - C++
  - jsharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9d7aa308-b667-48ed-b4c9-a61e49eb0a85
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MSBuild Conditions
[!INCLUDE[vstecmsbuild](../vs140/includes/vstecmsbuild_md.md)] supports a specific set of conditions that can be applied wherever a `Condition` attribute is allowed. The following table explains those conditions.  
  
|Condition|Description|  
|---------------|-----------------|  
|'`stringA`' == '`stringB`'|Evaluates to `true` if `stringA` equals `stringB`.<br /><br /> For example:<br /><br /> `Condition="'$(CONFIG)'=='DEBUG'"`<br /><br /> Single quotes are not required for simple alphanumeric strings or boolean values. However, single quotes are required for empty values.|  
|'`stringA`' != '`stringB`'|Evaluates to `true` if `stringA` is not equal to `stringB`.<br /><br /> For example:<br /><br /> `Condition="'$(CONFIG)'!='DEBUG'"`<br /><br /> Single quotes are not required for simple alphanumeric strings or boolean values. However, single quotes are required for empty values.|  
|<, >, <=, >=|Evaluates the numeric values of the operands. Returns `true` if the relational evaluation is true. Operands must evaluate to a decimal or hexadecimal number. Hexadecimal numbers must begin with "0x". **Note:**  In XML, the characters `<` and `>` must be escaped. The symbol `<` is represented as `<`. The symbol `>` is represented as `>`.|  
|Exists('`stringA`')|Evaluates to `true` if a file or folder with the name `stringA` exists.<br /><br /> For example:<br /><br /> `Condition="!Exists('$(builtdir)')"`<br /><br /> Single quotes are not required for simple alphanumeric strings or boolean values. However, single quotes are required for empty values.|  
|HasTrailingSlash('`stringA`')|Evaluates to `true` if the specified string contains either a trailing backward slash (\\) or forward slash (/) character.<br /><br /> For example:<br /><br /> `Condition="!HasTrailingSlash('$(OutputPath)')"`<br /><br /> Single quotes are not required for simple alphanumeric strings or boolean values. However, single quotes are required for empty values.|  
|!|Evaluates to `true` if the operand evaluates to `false`.|  
|And|Evaluates to `true` if both operands evaluate to `true`.|  
|Or|Evaluates to `true` if at least one of the operands evaluates to `true`.|  
|()|Grouping mechanism that evaluates to `true` if expressions contained inside evaluate to `true`.|  
|$if$ ( %expression% ), $else$, $endif$|Checks whether the specified `%expression%` matches the string value of the passed custom template parameter. If the `$if$` condition evaluates to `true`, then its statements are run; otherwise, the `$else$` condition is checked. If the `$else$` condition is `true`, then its statements are run; otherwise, the `$endif$` condition ends expression evaluation.<br /><br /> For examples of usage, see [Visual Studio Project/Item Template Parameter Logic](http://stackoverflow.com/questions/6709057/visual-studio-project-item-template-parameter-logic).|  
  
## See Also  
 [MSBuild Reference](../Topic/MSBuild%20Reference.md)   
 [MSBuild Conditional Constructs](../vs140/MSBuild-Conditional-Constructs.md)   
 [Walkthrough: Creating an MSBuild Project File from Scratch](../vs140/Walkthrough--Creating-an-MSBuild-Project-File-from-Scratch.md)