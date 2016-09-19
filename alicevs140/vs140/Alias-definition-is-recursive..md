---
title: "Alias definition is recursive."
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e48a2908-9b94-4c6a-9807-beeeba71531c
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Alias definition is recursive.
This error generally occurs when an alias has been defined that directly or indirectly references itself.  
  
### To correct this error  
  
1.  Change the definition of the alias and try again.  
  
     —or—  
  
2.  Review the current list of aliases and their definitions by entering `>alias` in the **Command** window and try again.  
  
## See Also  
 [Alias Command](../vs140/Alias-Command.md)   
 [Visual Studio Command Aliases](../vs140/Visual-Studio-Command-Aliases.md)