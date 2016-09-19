---
title: "Troubleshooting Exceptions: System.Data.StrongTypingException"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 90859ce2-3696-43cb-baf4-7daf98d8e2e1
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Troubleshooting Exceptions: System.Data.StrongTypingException
A <xref:System.Data.StrongTypingException?qualifyHint=False> occurs when the user accesses a <xref:System.DBNull?qualifyHint=False> value in a strongly typed <xref:System.Data.DataTable.DataSet?qualifyHint=False>.  
  
## Associated Tips  
 **Add error handling for the StrongTypingException.**  
 Place the code accessing the <xref:System.Data.DataTable.DataSet?qualifyHint=False> in a `Try…Catch` block and catch the <xref:System.Data.StrongTypingException?qualifyHint=False>.  
  
## See Also  
 <xref:System.Data.DataTable.DataSet?qualifyHint=False>   
 [How to: Find Out More About an Exception with the Exception Assistant](../Topic/How%20to:%20Use%20the%20Exception%20Assistant.md)   
 [Try...Catch...Finally Statement (Visual Basic)](../vs140/Try...Catch...Finally-Statement--Visual-Basic-.md)   
 [Datasets in Visual Studio Overview](assetId:///ee57f4f6-9fe1-4e0a-be9a-955c486ff427)