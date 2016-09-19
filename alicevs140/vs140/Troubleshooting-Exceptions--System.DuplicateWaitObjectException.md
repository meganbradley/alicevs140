---
title: "Troubleshooting Exceptions: System.DuplicateWaitObjectException"
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
ms.assetid: b9ff6932-a7cf-4a89-bd7d-e4ef1a3ff353
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Troubleshooting Exceptions: System.DuplicateWaitObjectException
A <xref:System.DuplicateWaitObjectException?qualifyHint=False> exception is thrown if the array of <xref:System.Threading.WaitHandle?qualifyHint=False> objects passed to <xref:System.Threading.WaitHandle.WaitAll?qualifyHint=False> or <xref:System.Threading.WaitHandle.WaitAny?qualifyHint=False> contains any duplicate operating system handles.  
  
## Associated Tips  
 **Make sure the WaitHandle objects passed to WaitAll or WaitAny are unique.**  
 A <xref:System.Threading.WaitHandle?qualifyHint=False> array cannot contain multiple references to the same object.  
  
### Remarks  
 The Common Language Runtime (CLR) provides a thread-synchronization mechanism based on synchronization objects waiting for execution in an array of <xref:System.Threading.WaitHandle?qualifyHint=False> objects.  
  
## See Also  
 <xref:System.DuplicateWaitObjectException?qualifyHint=False>   
 [How to: Find Out More About an Exception with the Exception Assistant](../Topic/How%20to:%20Use%20the%20Exception%20Assistant.md)