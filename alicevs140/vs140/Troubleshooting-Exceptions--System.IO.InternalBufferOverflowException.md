---
title: "Troubleshooting Exceptions: System.IO.InternalBufferOverflowException"
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
ms.assetid: 1f58ca15-c4e4-4af9-9a3d-42d2cf919cbe
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Troubleshooting Exceptions: System.IO.InternalBufferOverflowException
An <xref:System.IO.InternalBufferOverflowException?qualifyHint=False> exception is thrown when the internal buffer overflows.  
  
## Associated Tips  
 **When using FileSystemWatcher, filter out unwanted change notifications.**  
 In a file-system watcher, when you are notified of file changes, the system stores those changes in a buffer that the component creates and passes to the application programming interfaces (APIs). If there are many changes in a short time, the buffer can overflow, resulting in an <xref:System.IO.InternalBufferOverflowException?qualifyHint=False> exception, which loses all changes. To keep the buffer from overflowing, use the <xref:System.IO.FileSystemWatcher.NotifyFilter?qualifyHint=False> and <xref:System.IO.FileSystemWatcher.IncludeSubdirectories?qualifyHint=False> properties to filter out unwanted change notifications. For more information, see <xref:System.IO.FileSystemWatcher?qualifyHint=False>.  
  
## Remarks  
 You can also increase the size of the internal buffer through the <xref:System.IO.FileSystemWatcher.InternalBufferSize?qualifyHint=False> property. However, increasing the size of the buffer will affect performance, so it is best to keep the buffer as small as possible.  
  
## See Also  
 <xref:System.IO.InternalBufferOverflowException?qualifyHint=False>   
 [How to: Find Out More About an Exception with the Exception Assistant](../Topic/How%20to:%20Use%20the%20Exception%20Assistant.md)