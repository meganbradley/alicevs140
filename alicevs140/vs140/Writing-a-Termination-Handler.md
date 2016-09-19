---
title: "Writing a Termination Handler"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: language-reference
ms.assetid: 52aa1f8f-f8dd-44b8-be94-5e2fc88d44fb
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Writing a Termination Handler
Unlike an exception handler, a termination handler is always executed, regardless of whether the protected block of code terminated normally. The sole purpose of the termination handler should be to ensure that resources, such as memory, handles, and files, are properly closed regardless of how a section of code finishes executing.  
  
 Termination handlers use the try-finally statement.  
  
## What do you want to know more about?  
  
-   [The try-finally statement](../vs140/try-finally-Statement.md)  
  
-   [Cleaning up resources](../vs140/Cleaning-up-Resources.md)  
  
-   [Timing of actions in exception handling](../vs140/Timing-of-Exception-Handling--A-Summary.md)  
  
-   [Restrictions on termination handlers](../vs140/Restrictions-on-Termination-Handlers.md)  
  
## See Also  
 [Structured Exception Handling (C/C++)](../vs140/Structured-Exception-Handling--C-C---.md)