---
title: "Troubleshooting Exceptions: System.Reflection.AmbiguousMatchException"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f92b5c51-42b6-4c2e-83df-0d598b3b41c4
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Troubleshooting Exceptions: System.Reflection.AmbiguousMatchException
The exception that is thrown when binding to a method results in more than one method matching the binding criteria.  
  
## Remarks  
 An <xref:System.Reflection.AmbiguousMatchException?qualifyHint=False> is thrown if the application calls upon a class, and it cannot determine which class or overloaded class to use. The binding attempts to locate the proper class to use, determined by the number of parameters and the type of parameters. If multiple acceptable classes are located, this exception is thrown.  
  
## See Also  
 <xref:System.Reflection.AmbiguousMatchException?qualifyHint=False>   
 [How to: Find Out More About an Exception with the Exception Assistant](../Topic/How%20to:%20Use%20the%20Exception%20Assistant.md)