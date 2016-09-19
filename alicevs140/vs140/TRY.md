---
title: "TRY"
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
ms.topic: article
ms.assetid: a50dde15-8e3f-4747-a07f-ed09d342577c
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# TRY
Sets up a **TRY** block.  
  
## Syntax  
  
```  
  
TRY  
  
```  
  
## Remarks  
 A **TRY** block identifies a block of code that might throw exceptions. Those exceptions are handled in the following **CATCH** and `AND_CATCH` blocks. Recursion is allowed: exceptions may be passed to an outer **TRY** block, either by ignoring them or by using the `THROW_LAST` macro. End the **TRY** block with an `END_CATCH` or `END_CATCH_ALL` macro.  
  
 For more information, see the article [Exceptions](../vs140/Exception-Handling-in-MFC.md).  
  
## Example  
 See the example for [CATCH](../vs140/CATCH.md).  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [CATCH](../vs140/CATCH.md)   
 [AND_CATCH](../vs140/AND_CATCH.md)   
 [END_CATCH](../vs140/END_CATCH.md)   
 [CATCH_ALL](../vs140/CATCH_ALL.md)   
 [AND_CATCH_ALL](../vs140/AND_CATCH_ALL.md)   
 [END_CATCH_ALL](../vs140/END_CATCH_ALL.md)   
 [THROW](../vs140/THROW--MFC-.md)   
 [THROW_LAST](../vs140/THROW_LAST.md)