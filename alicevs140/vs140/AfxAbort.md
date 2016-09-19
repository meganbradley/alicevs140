---
title: "AfxAbort"
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
ms.assetid: c995759d-2326-4779-88e1-348d2b0bcecb
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxAbort
The default termination function supplied by MFC.  
  
## Syntax  
  
```  
  
void AfxAbort( );   
```  
  
## Remarks  
 `AfxAbort` is called internally by MFC member functions when there is a fatal error, such as an uncaught exception that cannot be handled. You can call `AfxAbort` in the rare case when you encounter a catastrophic error from which you cannot recover.  
  
## Example  
 See the example for [CATCH](../vs140/CATCH.md).  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)