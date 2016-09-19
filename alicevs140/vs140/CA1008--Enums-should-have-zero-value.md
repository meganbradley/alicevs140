---
title: "CA1008: Enums should have zero value"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-devops-test
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3503a73c-360c-416d-8ee4-c2aa44365a05
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CA1008: Enums should have zero value
|||  
|-|-|  
|TypeName|EnumsShouldHaveZeroValue|  
|CheckId|CA1008|  
|Category|Microsoft.Design|  
|Breaking Change|Non-breaking - When you are prompted to add a **None** value to a non-flag enumeration.Breaking - When you are prompted to rename or remove any enumeration values.|  
  
## Cause  
 An enumeration without an applied <xref:System.FlagsAttribute?qualifyHint=True> does not define a member that has a value of zero; or an enumeration that has an applied <xref:System.FlagsAttribute?qualifyHint=False> defines a member that has a value of zero but its name is not 'None', or the enumeration defines multiple zero-valued members.  
  
## Rule Description  
 The default value of an uninitialized enumeration, just like other value types, is zero. A non-flags−attributed enumeration should define a member that has the value of zero so that the default value is a valid value of the enumeration. If appropriate, name the member 'None'. Otherwise, assign zero to the most frequently used member. Note that, by default, if the value of the first enumeration member is not set in the declaration, its value is zero.  
  
 If an enumeration that has the <xref:System.FlagsAttribute?qualifyHint=False> applied defines a zero-valued member, its name should be 'None' to indicate that no values have been set in the enumeration. Using a zero-valued member for any other purpose is contrary to the use of the <xref:System.FlagsAttribute?qualifyHint=False> in that the AND and OR bitwise operators are useless with the member. This implies that only one member should be assigned the value zero. Note that if multiple members that have the value zero occur in a flags-attributed enumeration, `Enum.ToString()` returns incorrect results for members that are not zero.  
  
## How to Fix Violations  
 To fix a violation of this rule for non-flags−attributed enumerations, define a member that has the value of zero; this is a non-breaking change. For flags-attributed enumerations that define a zero-valued member, name this member 'None' and delete any other members that have a value of zero; this is a breaking change.  
  
## When to Suppress Warnings  
 Do not suppress a warning from this rule except for flags-attributed enumerations that have previously shipped.  
  
## Example  
 The following example shows two enumerations that satisfy the rule and an enumeration, `BadTraceOptions`, that violates the rule.  
  
 [!CODE [FxCop.Design.EnumsZeroValue#1](../CodeSnippet/VS_Snippets_CodeAnalysis/FxCop.Design.EnumsZeroValue#1)]  
  
## Related Rules  
 [Do not mark enums with FlagsAttribute](../Topic/CA2217:%20Do%20not%20mark%20enums%20with%20FlagsAttribute.md)  
  
 [Do not name enum values 'Reserved'](../vs140/CA1700--Do-not-name-enum-values--Reserved-.md)  
  
 [Do not prefix enum values with type name](../Topic/CA1712:%20Do%20not%20prefix%20enum%20values%20with%20type%20name.md)  
  
 [Enum Storage should be Int32](../Topic/CA1028:%20Enum%20storage%20should%20be%20Int32.md)  
  
 [Mark enums with FlagsAttribute](../Topic/CA1027:%20Mark%20enums%20with%20FlagsAttribute.md)  
  
## See Also  
 <xref:System.Enum?qualifyHint=True>