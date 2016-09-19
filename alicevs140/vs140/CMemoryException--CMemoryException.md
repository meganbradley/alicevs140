---
title: "CMemoryException::CMemoryException"
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
ms.assetid: 2adbea19-e8c5-4ad5-baf4-ad81d1d53c94
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMemoryException::CMemoryException
Constructs a `CMemoryException` object.  
  
## Syntax  
  
```  
  
CMemoryException( );  
```  
  
## Remarks  
 Do not use this constructor directly, but rather call the global function [AfxThrowMemoryException](../vs140/AfxThrowMemoryException.md). This global function can succeed in an out-of-memory situation because it constructs the exception object in previously allocated memory. For more information about exception processing, see the article [Exceptions](../vs140/Exception-Handling-in-MFC.md).  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CMemoryException Class](../vs140/CMemoryException-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [Exception Processing](../vs140/Exception-Processing.md)