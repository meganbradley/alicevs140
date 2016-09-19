---
title: "Lines View"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 71ec0781-6031-4e17-af09-f50226018437
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Lines View
The Lines view is available only for profiler data that was collected by using the sampling method. The view is not available for data that was collected by using instrumentation.  
  
 For sampling profile data, the Lines view identifies the statement in a function that was directly executing when the sample was collected. For .NET memory data, the Lines view identifies the statements that allocate memory.  
  
 In a source file, a statement can span more that one line in a source file, and a single line can include more than one statement.  
  
 A statement is identified by the following:  
  
-   The source file that contains the function statement.  
  
-   The function that contains the statement.  
  
-   The source line at which the statement starts.  
  
-   The character in the source line at which the statement starts.  
  
-   The source line at which the statement ends.  
  
-   The character in the source line at which the statement ends.  
  
## See Also  
 [Lines View - Profiler Sampling Data](../vs140/Lines-View---Sampling-Data.md)   
 [Lines View - Profiler .NET Memory Sampling Data](../vs140/Lines-View---.NET-Memory-Sampling-Data.md)   
 [Lines View - Profiler Contention Data](../vs140/Lines-View---Contention-Data.md)