---
title: "Troubleshooting Exceptions: System.Drawing.Printing.InvalidPrinterException"
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
ms.assetid: e19b9b9c-2b0f-4839-85c0-ae75e1c356d2
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Troubleshooting Exceptions: System.Drawing.Printing.InvalidPrinterException
An <xref:System.Drawing.Printing.InvalidPrinterException?qualifyHint=False> exception is thrown when an attempt is made to access a printer using invalid printer settings.  
  
## Associated Tips  
 **Make sure that the printer exists.**  
 The most common cause of invalid printer settings is referencing a nonexistent printer. For more information, see <xref:System.Drawing.Printing?qualifyHint=False>.  
  
 **Make sure a default printer has been installed.**  
 If no printer has been specified, make sure a default printer has been installed. For more information, see <xref:System.Drawing.Printing.PrintDocument.PrinterSettings?qualifyHint=False>  
  
## See Also  
 <xref:System.Drawing.Printing.InvalidPrinterException?qualifyHint=False>   
 <xref:System.Drawing.Printing.PrinterSettings?qualifyHint=False>   
 [How to: Find Out More About an Exception with the Exception Assistant](../Topic/How%20to:%20Use%20the%20Exception%20Assistant.md)