---
title: "Troubleshooting Exceptions: System.IO.EndOfStreamException"
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
ms.assetid: 1271e6f6-3a0d-49f0-9ff4-178d480687be
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Troubleshooting Exceptions: System.IO.EndOfStreamException
An <xref:System.IO.EndOfStreamException?qualifyHint=False> exception is thrown when there is an attempt to read past the end of a stream.  
  
## Associated Tips  
 **Check whether the end of the file has been reached before reading.**  
 Use the <xref:System.IO.StreamReader.Peek?qualifyHint=False> method to check the end of the file before reading from the stream.  
  
## See Also  
 <xref:System.IO.EndOfStreamException?qualifyHint=False>   
 [How to: Find Out More About an Exception with the Exception Assistant](../Topic/How%20to:%20Use%20the%20Exception%20Assistant.md)   
 [Reading and Writing to a Newly Created Data File](assetId:///e209d949-31e8-44ea-8e38-87f9093f3093)   
 [Opening and Appending to a Log File](assetId:///74423362-1721-49cb-aa0a-e04005f72a06)