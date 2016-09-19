---
title: "Troubleshooting Exceptions: System.Threading.SynchronizationLockException"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 82d80643-fc5c-40ae-a579-46869772d25c
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Troubleshooting Exceptions: System.Threading.SynchronizationLockException
The exception that is thrown when a method requires the caller to own the lock on a given `Monitor`, and the method is invoked by a caller that does not own that lock.  
  
## Remarks  
 A <xref:System.Threading.SynchronizationLockException?qualifyHint=False> is thrown by calling the <xref:System.Threading.Monitor.Exit?qualifyHint=False>, <xref:System.Threading.Monitor.Pulse?qualifyHint=False>, <xref:System.Threading.Monitor.PulseAll?qualifyHint=False>, and <xref:System.Threading.Monitor.Wait?qualifyHint=False> methods of the `Monitor` class from an unsynchronized block of code.  
  
## See Also  
 <xref:System.Threading.SynchronizationLockException?qualifyHint=False>   
 [How to: Find Out More About an Exception with the Exception Assistant](../Topic/How%20to:%20Use%20the%20Exception%20Assistant.md)