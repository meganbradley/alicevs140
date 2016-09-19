---
title: "Troubleshooting Exceptions: System.OperationCanceledException"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 275e2887-7491-432b-9b80-a21bb794be29
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Troubleshooting Exceptions: System.OperationCanceledException
An <xref:System.OperationCanceledException?qualifyHint=False> is thrown when an operation is made with the <xref:Microsoft.VisualBasic.FileIO.UICancelOption?qualifyHint=False> set to `ThrowException` and the operation is cancelled.  
  
## Associated Tips  
 If you would prefer that this exception not be thrown, set <xref:System.OperationCanceledException?qualifyHint=False> to `DoNothing`.  
 <xref:Microsoft.VisualBasic.FileIO.UICancelOption?qualifyHint=False> has a default value of `ThrowException`. If you do not wish this exception to be thrown when the user cancels the operation, set the enumeration value to `DoNothing`.  
  
## See Also  
 <xref:System.OperationCanceledException?qualifyHint=False>   
 [How to: Find Out More About an Exception with the Exception Assistant](../Topic/How%20to:%20Use%20the%20Exception%20Assistant.md)