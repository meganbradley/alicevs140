---
title: "Troubleshooting Exceptions: Microsoft.Office.Tools.CannotRemoveControlException"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - JScript
  - VB
  - CSharp
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0c806cb7-b34b-4664-999b-4621efd97414
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Troubleshooting Exceptions: Microsoft.Office.Tools.CannotRemoveControlException
A <xref:Microsoft.Office.Tools.CannotRemoveControlException?qualifyHint=False> exception is thrown when an attempt is made to programmatically remove a control that was not added programmatically.  
  
## Associated Tips  
 You can only remove a control programmatically if it was added programmatically.  
 -   You can only remove a control programmatically if it was added programmatically. If the control was added to the document at design time instead of at run time, it cannot be removed.  
  
## See Also  
 <xref:Microsoft.Office.Tools.CannotRemoveControlException?qualifyHint=False>   
 [How to: Find Out More About an Exception with the Exception Assistant](../Topic/How%20to:%20Use%20the%20Exception%20Assistant.md)