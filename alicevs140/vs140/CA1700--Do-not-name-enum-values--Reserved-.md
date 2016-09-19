---
title: "CA1700: Do not name enum values &#39;Reserved&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-devops-test
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7a7e01c3-ae7d-4c82-a646-91b58864a749
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CA1700: Do not name enum values &#39;Reserved&#39;
|||  
|-|-|  
|TypeName|DoNotNameEnumValuesReserved|  
|CheckId|CA1700|  
|Category|Microsoft.Naming|  
|Breaking Change|Breaking|  
  
## Cause  
 The name of an enumeration member contains the word "reserved".  
  
## Rule Description  
 This rule assumes that an enumeration member that has a name that contains "reserved" is not currently used but is a placeholder to be renamed or removed in a future version. Renaming or removing a member is a breaking change. You should not expect users to ignore a member just because its name contains "reserved", nor can you rely on users to read or abide by documentation. Furthermore, because reserved members appear in object browsers and smart integrated development environments, they can cause confusion about which members are actually being used.  
  
 Instead of using a reserved member, add a new member to the enumeration in the future version. In most cases the addition of the new member is not a breaking change, as long as the addition does not cause the values of the original members to change.  
  
 In a limited number of cases the addition of a member is a breaking change even when the original members retain their original values. Primarily, the new member cannot be returned from existing code paths without breaking callers that use a `switch` (`Select` in [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)]) statement on the return value that encompasses the whole member list and that throw an exception in the default case. A secondary concern is that client code might not handle the change in behavior from reflection methods such as <xref:System.Enum.IsDefined?qualifyHint=True>. Accordingly, if the new member has to be returned from existing methods or a known application incompatibility occurs because of poor reflection usage, the only nonbreaking solution is to:  
  
1.  Add a new enumeration that contains the original and new members.  
  
2.  Mark the original enumeration with the <xref:System.ObsoleteAttribute?qualifyHint=True> attribute.  
  
 Follow the same procedure for any externally visible types or members that expose the original enumeration.  
  
## How to Fix Violations  
 To fix a violation of this rule, remove or rename the member.  
  
## When to Suppress Warnings  
 It is safe to suppress a warning from this rule for a member that is currently used or for libraries that have previously shipped.  
  
## Related Rules  
 [Do not mark enums with FlagsAttribute](../Topic/CA2217:%20Do%20not%20mark%20enums%20with%20FlagsAttribute.md)  
  
 [Do not prefix enum values with type name](../Topic/CA1712:%20Do%20not%20prefix%20enum%20values%20with%20type%20name.md)  
  
 [Enum Storage should be Int32](../Topic/CA1028:%20Enum%20storage%20should%20be%20Int32.md)  
  
 [Enums should have zero value](../vs140/CA1008--Enums-should-have-zero-value.md)  
  
 [Mark enums with FlagsAttribute](../Topic/CA1027:%20Mark%20enums%20with%20FlagsAttribute.md)