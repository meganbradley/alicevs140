---
title: "Troubleshooting Exceptions: System.Printing.PrintingCanceledException"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bec418d6-f168-4a73-962f-5ee0427600b6
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Troubleshooting Exceptions: System.Printing.PrintingCanceledException
A <xref:System.Printing.PrintingCanceledException?qualifyHint=False> exception occurs when code attempts to access a canceled print job.  
  
## Remarks  
 If you are creating a Windows Presentation Foundation (WPF) application that includes printing functionality and allows print jobs to be canceled, be sure to correctly handle this exception. An unhandled exception of this type can cause a Windows Presentation Foundation application to stop responding.  
  
## See Also  
 <xref:System.Printing.PrintingCanceledException?qualifyHint=False>   
 [How to: Find Out More About an Exception with the Exception Assistant](../Topic/How%20to:%20Use%20the%20Exception%20Assistant.md)