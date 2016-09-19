---
title: "AfxThrowMemoryException"
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
ms.assetid: 1c280bfd-6ccf-4b1d-8614-3eaa005cada4
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxThrowMemoryException
Throws a memory exception.  
  
## Syntax  
  
```  
  
void AfxThrowMemoryException( );  
```  
  
## Remarks  
 Call this function if calls to underlying system memory allocators (such as `malloc` and the [GlobalAlloc](http://msdn.microsoft.com/library/windows/desktop/aa366574) Windows function) fail. You do not need to call it for **new** because **new** will throw a memory exception automatically if the memory allocation fails.  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [CMemoryException Class](../vs140/CMemoryException-Class.md)   
 [THROW](../vs140/THROW--MFC-.md)