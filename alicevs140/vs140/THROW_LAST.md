---
title: "THROW_LAST"
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
ms.assetid: a4ca8efc-239d-4da3-add9-c29c82bff338
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# THROW_LAST
Throws the exception back to the next outer **CATCH** block.  
  
## Syntax  
  
```  
  
THROW_LAST( )  
```  
  
## Remarks  
 This macro allows you to throw a locally created exception. If you try to throw an exception that you have just caught, it will normally go out of scope and be deleted. With `THROW_LAST`, the exception is passed correctly to the next **CATCH** handler.  
  
 For more information, see the article [Exceptions](../vs140/Exception-Handling-in-MFC.md).  
  
## Example  
 See the example for [CFile::Abort](../vs140/CFile--Abort.md).  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [THROW](../vs140/THROW--MFC-.md)   
 [TRY](../vs140/TRY.md)   
 [CATCH](../vs140/CATCH.md)   
 [AND_CATCH](../vs140/AND_CATCH.md)   
 [END_CATCH](../vs140/END_CATCH.md)   
 [CATCH_ALL](../vs140/CATCH_ALL.md)   
 [AND_CATCH_ALL](../vs140/AND_CATCH_ALL.md)   
 [END_CATCH_ALL](../vs140/END_CATCH_ALL.md)