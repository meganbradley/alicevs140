---
title: "CA1702: Compound words should be cased correctly"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-devops-test
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 05481245-7ad8-48c3-a456-3aa44b6160a6
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CA1702: Compound words should be cased correctly
|||  
|-|-|  
|TypeName|CompoundWordsShouldBeCasedCorrectly|  
|CheckId|CA1702|  
|Category|Microsoft.Naming|  
|Breaking Change|Breaking- when fired on assemblies.<br /><br /> Non-breaking - when fired on type parameters.|  
  
## Cause  
 The name of an identifier contains multiple words and at least one of the words appears to be a compound word that is not cased correctly.  
  
## Rule Description  
 The name of the identifier is split into words that are based on the casing. Each contiguous two-word combination is checked by the Microsoft spelling checker library. If it is recognized, the identifier produces a violation of the rule. Examples of compound words that cause a violation are "CheckSum" and "MultiPart", which should be cased as "Checksum" and "Multipart", respectively. Due to previous common usage, several exceptions are built into the rule, and several single words are flagged, such as "Toolbar" and "Filename", that should be cased as two distinct words (in this case, "ToolBar" and "FileName").  
  
 Naming conventions provide a common look for libraries that target the common language runtime. This reduces the learning curve that is required for new software libraries, and increases customer confidence that the library was developed by someone who has expertise in developing managed code.  
  
## How to Fix Violations  
 Change the name so that it is cased correctly.  
  
## When to Suppress Warnings  
 It is safe to suppress a warning from this rule if both parts of the compound word are recognized by the spelling dictionary and the intent is to use two words.  
  
## Related Rules  
 [Resource string compound words should be cased correctly](../vs140/CA1701--Resource-string-compound-words-should-be-cased-correctly.md)  
  
 [Identifiers should be cased correctly](../vs140/CA1709--Identifiers-should-be-cased-correctly.md)  
  
 [Identifiers should differ by more than case](../vs140/CA1708--Identifiers-should-differ-by-more-than-case.md)  
  
## See Also  
 [Guidelines for Names](assetId:///fc076d66-9b5f-42d3-aa65-61d970c794a3)   
 [Capitalization Conventions](assetId:///4c4ea526-9203-486f-b72d-29d61c5b3c6d)