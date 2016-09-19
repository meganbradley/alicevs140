---
title: "CA2237: Mark ISerializable types with SerializableAttribute"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-devops-test
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9bd6bb24-a527-43dd-9952-043c0c694f46
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CA2237: Mark ISerializable types with SerializableAttribute
|||  
|-|-|  
|TypeName|MarkISerializableTypesWithSerializable|  
|CheckId|CA2237|  
|Category|Microsoft.Usage|  
|Breaking Change|Non Breaking|  
  
## Cause  
 An externally visible type implements the <xref:System.Runtime.Serialization.ISerializable?qualifyHint=True> interface and the type is not marked with the <xref:System.SerializableAttribute?qualifyHint=True> attribute. The rule ignores derived types whose base type is not serializable.  
  
## Rule Description  
 To be recognized by the common language runtime as serializable, types must be marked with the <xref:System.SerializableAttribute?qualifyHint=False> attribute even if the type uses a custom serialization routine through implementation of the <xref:System.Runtime.Serialization.ISerializable?qualifyHint=False> interface.  
  
## How to Fix Violations  
 To fix a violation of this rule, apply the <xref:System.SerializableAttribute?qualifyHint=False> attribute to the type.  
  
## When to Suppress Warnings  
 Do not suppress a warning from this rule for exception classes because they must be serializable to work correctly across application domains.  
  
## Example  
 The following example shows a type that violates the rule. Uncomment the <xref:System.SerializableAttribute?qualifyHint=False> attribute line to satisfy the rule.  
  
 [!CODE [FxCop.Usage.MarkSerializable#1](../CodeSnippet/VS_Snippets_CodeAnalysis/FxCop.Usage.MarkSerializable#1)]  
  
## Related Rules  
 [Call base class methods on ISerializable types](../Topic/CA2236:%20Call%20base%20class%20methods%20on%20ISerializable%20types.md)  
  
 [Implement ISerializable correctly](../Topic/CA2240:%20Implement%20ISerializable%20correctly.md)  
  
 [Implement serialization constructors](../Topic/CA2229:%20Implement%20serialization%20constructors.md)  
  
 [Implement serialization methods correctly](../Topic/CA2238:%20Implement%20serialization%20methods%20correctly.md)  
  
 [Mark all non-serializable fields](../Topic/CA2235:%20Mark%20all%20non-serializable%20fields.md)  
  
 [Provide deserialization methods for optional fields](../Topic/CA2239:%20Provide%20deserialization%20methods%20for%20optional%20fields.md)  
  
 [Secure serialization constructors](../Topic/CA2120:%20Secure%20serialization%20constructors.md)