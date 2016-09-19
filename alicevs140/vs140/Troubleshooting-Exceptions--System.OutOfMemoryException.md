---
title: "Troubleshooting Exceptions: System.OutOfMemoryException"
ms.custom: na
ms.date: 09/19/2016
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
ms.assetid: eb16f008-964e-40a1-91f6-6ad25fa82d5a
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Troubleshooting Exceptions: System.OutOfMemoryException
An <xref:System.OutOfMemoryException?qualifyHint=False> exception is thrown when an attempt to allocate memory fails.  
  
## Associated Tips  
 **If you are creating an array, make sure the size is correct.**  
 For more information, Visual Basic users can see [Arrays in Visual Basic](../Topic/Arrays%20in%20Visual%20Basic.md).  
  
 For more information, C# users can see [Arrays (C# Programmer's Reference)](../Topic/Arrays%20\(C%23%20Programming%20Guide\).md).  
  
 **Be sure you have enough memory for internal purposes and new managed objects.**  
 If you are programming on the [!INCLUDE[Compact](../vs140/includes/compact_md.md)], the common language runtime throws this exception when there is not enough memory for internal purposes or new managed objects. To prevent the exception, avoid programming large methods that consume 64 or more kilobytes of memory.  
  
## Remarks  
 Excessive managed memory usage is commonly caused by:  
  
-   Reading large data sets into memory.  
  
-   Creating excessive cache entries.  
  
-   Uploading or downloading large files.  
  
-   Excessive use of regular expressions or strings while parsing files.  
  
-   Excessive view state.  
  
-   Too much data in session state or too many sessions.  
  
 This exception may be thrown with an additional message, "Not enough storage is available to complete this operation," when invoking a method on a COM object that returns a user-defined type that contains a safe array (an array of non-fixed size). This is because the .NET Framework cannot marshal a structure field with a safe array type.  
  
## See Also  
 <xref:System.OutOfMemoryException?qualifyHint=False>   
 [How to: Find Out More About an Exception with the Exception Assistant](../Topic/How%20to:%20Use%20the%20Exception%20Assistant.md)