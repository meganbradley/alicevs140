---
title: "CA1703: Resource strings should be spelled correctly"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-devops-test
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 693f4970-f512-40cb-ae3b-a0f3a5c6d6f1
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CA1703: Resource strings should be spelled correctly
|||  
|-|-|  
|TypeName|ResourceStringsShouldBeSpelledCorrectly|  
|CheckId|CA1703|  
|Category|Microsoft.Naming|  
|Breaking Change|Non-breaking|  
  
## Cause  
 A resource string contains one or more words that are not recognized by the Microsoft spelling checker library.  
  
## Rule Description  
 This rule parses the resource string into words (tokenizing compound words) and checks the spelling of each word/token. For information about the parsing algorithm, see [Identifiers should be spelled correctly](../vs140/CA1704--Identifiers-should-be-spelled-correctly.md).  
  
 By default, the English (en) version of the spelling checker is used.  
  
## How to Fix Violations  
 To fix a violation of this rule, use complete words that are correctly spelled or add the words to a custom dictionary. For information about how to use custom dictionaries, see [Identifiers should be spelled correctly](../vs140/CA1704--Identifiers-should-be-spelled-correctly.md).  
  
## When to Suppress Warnings  
 Do not suppress a warning from this rule. Correctly spelled words reduce the time that is required to learn new software libraries.  
  
## Related Rules  
 [Resource string compound words should be cased correctly](../vs140/CA1701--Resource-string-compound-words-should-be-cased-correctly.md)  
  
 [Identifiers should be spelled correctly](../vs140/CA1704--Identifiers-should-be-spelled-correctly.md)  
  
 [Literals should be spelled correctly](../Topic/CA2204:%20Literals%20should%20be%20spelled%20correctly.md)