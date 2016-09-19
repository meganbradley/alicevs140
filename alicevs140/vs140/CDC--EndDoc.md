---
title: "CDC::EndDoc"
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
ms.topic: reference
ms.assetid: f3de0ffc-dd85-4bdb-8a8c-eb4cc4c0ca62
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::EndDoc
Ends a print job started by a call to the [StartDoc](../vs140/CDC--StartDoc.md) member function.  
  
## Syntax  
  
```  
  
int EndDoc( );  
```  
  
## Return Value  
 Greater than or equal to 0 if the function is successful, or a negative value if an error occurred.  
  
## Remarks  
 This member function replaces the **ENDDOC** printer escape, and should be called immediately after finishing a successful print job.  
  
 If an application encounters a printing error or a canceled print operation, it must not attempt to terminate the operation by using either `EndDoc` or [AbortDoc](../vs140/CDC--AbortDoc.md). GDI automatically terminates the operation before returning the error value.  
  
 This function should not be used inside metafiles.  
  
## Example  
 See the example for [CDC::StartDoc](../vs140/CDC--StartDoc.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::AbortDoc](../vs140/CDC--AbortDoc.md)   
 [CDC::Escape](../vs140/CDC--Escape.md)   
 [CDC::StartDoc](../vs140/CDC--StartDoc.md)