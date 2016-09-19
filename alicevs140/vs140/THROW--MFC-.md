---
title: "THROW (MFC)"
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
ms.assetid: 794b8de1-bf90-4877-b96a-bc7b17b1e460
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# THROW (MFC)
Throws the specified exception.  
  
## Syntax  
  
```  
  
THROW(  
exception_object_pointer )  
```  
  
#### Parameters  
 *exception_object_pointer*  
 Points to an exception object derived from `CException`.  
  
## Remarks  
 **THROW** interrupts program execution, passing control to the associated **CATCH** block in your program. If you have not provided the **CATCH** block, then control is passed to a Microsoft Foundation Class Library module that prints an error message and exits.  
  
 For more information, see the article [Exceptions](../vs140/Exception-Handling-in-MFC.md).  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [THROW_LAST](../vs140/THROW_LAST.md)   
 [TRY](../vs140/TRY.md)   
 [CATCH](../vs140/CATCH.md)   
 [AND_CATCH](../vs140/AND_CATCH.md)   
 [END_CATCH](../vs140/END_CATCH.md)   
 [CATCH_ALL](../vs140/CATCH_ALL.md)   
 [AND_CATCH_ALL](../vs140/AND_CATCH_ALL.md)   
 [END_CATCH_ALL](../vs140/END_CATCH_ALL.md)   
 [AfxThrowArchiveException](../vs140/AfxThrowArchiveException.md)   
 [AfxThrowFileException](../vs140/AfxThrowFileException.md)   
 [AfxThrowMemoryException](../vs140/AfxThrowMemoryException.md)   
 [AfxThrowNotSupportedException](../vs140/AfxThrowNotSupportedException.md)   
 [AfxThrowResourceException](../vs140/AfxThrowResourceException.md)   
 [AfxThrowUserException](../vs140/AfxThrowUserException.md)